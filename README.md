# Worksheets
```au3
_Example() Func _Example()      
Local $oErrorHandler = ObjEvent("AutoIt.Error", "_ErrFunc")    
#forceref $oErrorHandler  
;---- From https://scand.com/products/gspread/    
; $sName - User name, any you like    
; $sClientIdAndSecret - "client_id|client_secret" format    
; example client id: 292085223830.apps.googleusercontent.com    
; $sScriptId - Google Apps script ID    
; https://docs.microsoft.com/en-us/office/vba/api/excel.application.maillogon    
$sName = "Owner"    
$sClientIdAndSecret = "myclientidString|myclientSecret" 
; from generate client_id.json    
$sScriptId = "myappscriptidString"       
Local $oApp = ObjCreate("GSpreadCOM.Application")    
$oApp.MailLogon($sName, $sClientIdAndSecret, $sScriptId)    
;$oApp.Workbooks.Item("Example2").Worksheets.Item("Sheet1").Activate()  
EndFunc   
;==>_Example
```
