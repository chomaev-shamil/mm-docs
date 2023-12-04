## Routes for app [iOS]

#### Auth (phone + otp)
- ``/auth (obtain, etc..)``

#### Donations
- ``/donations ?region_id, category_id, organization_id, status, is_report != null, is_favorite``
- ``/donations/:id``
- ``/donations/:id/report [.post]``
- ``/donations/:id/donate [.post > (type: one-time, amount: 314)]``

#### Donation comments
- ``/donations/:id/comments/``
- ``/donations/:id/comments/ [.post]``
- ``/donations/:id/comments/:id/report [.post]``

#### Users
- ``/users/me``
- ``/users/me [.patch]``
- ``/users/me [.delete]``

#### Region (for filters)
- ``/regions``
- ``/regions/:id``

#### Categories (for filters)
- ``/categories``
- ``/categories/:id``

#### Organizations
- ``/organizations``
- ``/organizations/:id``
- ``/organizations/:id/donate [.post > (amount: 314)]``
- ``/organizations/:id/subscribe [.post > (amount: 314)]``

###### Или можем использовать этот запрос
- ``/organizations/:id/donate [.post > (type: monthly/one-time, amount: 314)]``

#### Notifications tokens
- ``/notification-tokens [.post]``
- ``/notification-tokens [.patch]``
- ``/notification-tokens [.delete]``

#### Subscriptions
- ``/subscriptions/my``
- ``/subscriptions/:id``
- ``/subscriptions/:id/cancel [.post] // or use .delete``

#### Payments
###### Может этот запрос не нужен, обсудим
- ``/payments/my ``
