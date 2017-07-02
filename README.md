# Angularjs-Category-Lists-count

You can use groupBy of angular.filter module.
so you can do something like this:

JS

    var app = angular.module('catApp', ['angular.filter']);

    app.controller('blogCtrl', function($scope, $rootScope) {
    $rootScope.blogposts = [
        {
          post_title : 'Alfreds Futterkiste',
          post_category : 'social'
        },
        {
          post_title : 'Ana Trujillo Emparedados y helados',
          post_category : 'social'
        },
        {
          post_title : 'Antonio Moreno Taquería',
          post_category : 'news'
        },
        {
          post_title : 'Around the Horn',
          post_category : 'news'
        },
        {
          post_title : 'B Beverages',
          post_category : 'social'
        },
        {
          post_title : 'Berglunds snabbköp',
          post_category : 'social'
        },
        {
          post_title : 'Blauer See Delikatessen',
          post_category : 'business'
        },
        {
          post_title : 'Blondel père et fils',
          post_category : 'business'
        },
        {
          post_title : 'Bólido Comidas preparadas',
          post_category : 'business'
        },
        {
          post_title : 'Bon app',
          post_category : 'health'
        },
        {
          post_title : 'Bottom-Dollar Marketse',
          post_category : 'business'
        },
        {
          post_title : 'Cactus Comidas para llevar',
          post_category : 'health'
        },
        {
          post_title : 'Centro comercial Moctezuma',
          post_category : 'business'
        },
        {
          post_title : 'Chop-suey Chinese',
          post_category : 'business'
        },
        {
          post_title : 'Comércio Mineiro',
          post_category : 'health'
        }
      ];

      });
      
HTML

    <ul>
        <li ng-repeat="(key, value) in blogposts | groupBy: 'post_category'">{{key}} <span>{{value.length}}</span></li>
      </ul>
