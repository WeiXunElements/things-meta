# things-entity-meta

## Entity 기반의 화면 자동 구성을 위한 데이터를 제공하기 위한 메타 정보용 컴포넌트

Entity 기반의 화면은 검색 조건과 그리드로 구성된다.<br/>
검색 조건과 그리드는 서버로 부터 받아온 메타 정보를 바탕으로 자동으로 구성되는데 이를 위해서 서버로 부터 설정한 Entity에 대한 메타 정보를 조회하여 화면 자동 구성을 위한 데이터를 조회하기 위한 메타 정보용 컴포넌트이다.

Example:

```html
    <things-entity-meta 
        id="resourceMeta" 
        resource-type="Role" 
        sort-fields = "{{sortFields}}"
        select-fields="{{selectFields}}"
        search-form-fields ="{{searchFormFields}}"
        resource-form-fields ="{{resourceFormFields}}"
        grid-model ="{{gridModel}}"
        grid-columns ="{{gridColumns}}">
    </things-entity-meta>
```

```js
    this.$['resourceMeta'].loadMeta();
```
# things-menu-meta

## Menu 기반의 화면 자동 구성을 위한 데이터를 셋업하기 위한 메타 정보용 컴포넌트.

기본적인 Menu 기반의 화면은 검색 조건과 그리드, 버튼 그리고 상세 폼으로 구성된다.<br/>
검색 조건과 그리드, 상세폼, 버튼 정보는 서버로 부터 받아온 메타 정보를 바탕으로 자동으로 구성되는데 이를 위해서 서버로 부터 설정한 MenuId로 메뉴에 대한 메타 정보를 조회하여 화면 자동 구성을 위한 데이터를 제공하기 위한 메타 정보용 컴포넌트이다.

Example:

```html
    <things-menu-meta 
        id="resourceMeta" 
        menu-id="5" 
        sort-fields = "{{sortFields}}"
        select-fields="{{selectFields}}"
        search-form-fields ="{{searchFormFields}}"
        resource-form-fields ="{{resourceFormFields}}"
        grid-model ="{{gridModel}}"
        grid-columns ="{{gridColumns}}">
    </things-menu-meta>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install

## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polymer-cli

And you can run it via:

    polymer serve

Once running, you can preview your element at
`http://localhost:8080/components/things-alarm/`, where `things-alarm` is the name of the directory containing it.
