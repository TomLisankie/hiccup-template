### hiccup-template

A minimal Clojure/Script library for Hiccup style templating.

### usage

```clojure
(require '[hiccup-template.core :as ht])

(def data
 {:person
  {:first-name "John"
   :last-name "Doe"}})

 (def template
   [:div
    [:label "first name " :data/person.first-name]
    [:label "last name " :data/person.last-name]])

(ht/hiccup template data)
; [:div [:label "first name " "John"] [:label "last name " "Doe"]]

(ht/html template data)
; <div><label>first name John</label><label>last name Doe</label></div>
```