## axiosの使い方

### axiosのデフォルトグローバルの設定
```js

axios.defaults.baseURL = 'https://jsonplaceholder.typicode.com';
axios.defaults.headers.common['Authorization'] - 'AUTH TOKEN';
axios.defaults.headers.post['Content-Type'] = 'application/json';


axios.interceptors.request.use(request => {
  console.log(request);
  return request;
}, error => {
  console.log(error);
  return Promise.reject(error);
});

axios.interceptors.response.use(request => {
  console.log(request);
  return request;
}, error => {
  console.log(error);
  return Promise.reject(error);
});

//これで各,componentにパスを書かなくても大丈夫
```
