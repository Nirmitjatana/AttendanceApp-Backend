# DevGuide

## To help someone who will work on this in future, To help the frontend person:(This may not be exactly True)

- when a new event is created, event-name (slug) is added in events db. Now when attende sends otp we take it and check if it matches with any
event and event attendence is going on. Then we take attendence and emit this info to admin namespace.
- also, attende attendence is sended to one more route that attendence is emited to that particular event room (if allowed for so by admin).
attendence is emitted to:

1) attendence namespace, from their attendence is done and emited to admin.
2) broadcaster namespace, from there to specific room name if allowed by admin.

- admin_namespace -> to emit to the admin_namespace :emits to the client side namespace then  (SERVER SIDE NOT NEEDED)
- attendence_namespace-> attendence (to emit client attendence) :emits to the client side admin_namespace then
- broadcaster_namespace -> attendence comes to this namespace also, from here it's sended to particular room

## Not doing (Improvements/edge-bug)

- replace flask-jwt with flask-jwt-extended
- empty password is allowed :) Yes, Auth is just to keep users track
- only single ip connection allowed for 1 user
- clean datetime.datetime.now()
- check bugs for sockets
- jwt token expiry thing api
- add distance field in Attendence Model
- handle socket exceptions, use get for dict and seal with catch blocks
- attendence route is handling error but very less informatic to client, can be improved
- Fix spelling of Attendance
- When admin marks attendance, then ad a new filed to keep this record
- login with linkden
- generalize api returns
- add status code to all sockets and make their pattern very much same
- add recaptcha
- Forgot password
- Change Password
