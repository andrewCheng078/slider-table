
## 需求
```js

$('.frzTable.default').frzTable({
    count: {
        // M版時每次點擊往前往後移動幾格儲存格
        slide: 1, // [number] 
        // M版時一個畫面show幾格儲存格
        show: 4 // [number] 
    },
    // 設定花多久時間移動完成
    speed: .3, // [number] 
    // 每次點擊儲存格時會執行此callback，並帶入所點擊的儲存格jquery物件
    whenClick: function($element) {
        // console.log($element)
    }
})
$('.frzTable.rel').frzTable({
    count: {
        slide: 1,
        show: 2
    },
    whenClick: function($element) {
        // console.log($element)
    }
})

```

## note
   

1. ~~手機板 min-width 以手機板大小為主~~
2. ~~不要再js裡寫計算css~~
3. ~~prop決定出現幾個格子~~
4. ~~點箭頭移動幾個儲存格~~
5. ~~RWD轉換HTML要用同一個~~
6. ~~移動端 調整過日期 拉回pc版要保存上次的狀態~~
~~456 > 123456 > 456~~
7. ~~css點擊後會劃十字 用餘數(目前為dom操作,待改(用資料操作))~~
8. ~~表個 各定 7 天~~
9. ~~移動時要用class~~
10. ~~callback( ) => console.log()可以自己打東西 註冊在window底下~~

```js

   if(this.state.show === 1){
                if(this.state.slide === 1){
                    if(this.state.count === 5){this.setState({R_ButtonHide:false,})};
                    this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`});
                }

                if(this.state.slide === 2){
                    if(this.state.count === 4){this.setState({R_ButtonHide:false,})};
                    this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`});
                      
                }

                if(this.state.slide === 3){
                    if(this.state.count >=3){this.setState({R_ButtonHide:false,})};
                    this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`});
                      
                }

                if(this.state.slide === 4){
                    if(this.state.count >=4){this.setState({R_ButtonHide:false,moveClass:`move-1-${this.state.count+=2}`})}else{
                        this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`});
                    };  
                }

                if(this.state.slide === 5){
                    if(this.state.count >=5){this.setState({R_ButtonHide:false,moveClass:`move-1-${this.state.count+=1}`})}else{
                        this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`});
                    };  
                }

                if(this.state.slide === 6){
                        this.setState({moveClass:`move-1-${this.state.count+=this.state.slide}`,R_ButtonHide:false,});
                }

            }
            this.setState({L_ButtonHide:true,})

```


## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

