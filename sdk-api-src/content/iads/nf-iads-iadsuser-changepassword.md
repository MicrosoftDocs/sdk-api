---
UID: NF:iads.IADsUser.ChangePassword
title: IADsUser::ChangePassword (iads.h)
author: windows-sdk-content
description: Changes the user password from the specified old value to a new value.
old-location: adsi\iadsuser_changepassword.htm
tech.root: adsi
ms.assetid: 279087b1-450a-4089-a5f6-257849ae583f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ChangePassword, ChangePassword method [ADSI], ChangePassword method [ADSI],IADsUser interface, IADsUser interface [ADSI],ChangePassword method, IADsUser.ChangePassword, IADsUser::ChangePassword, _ds_iadsuser_changepassword, adsi.iadsuser__changepassword, adsi.iadsuser_changepassword, iads/IADsUser::ChangePassword
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsUser.ChangePassword
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsUser::ChangePassword


## -description


The <b>IADsUser::ChangePassword</b> method changes the user password from the specified old value to a new value.


## -parameters




### -param bstrOldPassword [in]

A <b>BSTR</b> that contains the current password.


### -param bstrNewPassword [out]

A <b>BSTR</b> that contains the new password.


## -returns



This method supports the standard return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



<b>IADsUser::ChangePassword</b> functions similarly to <a href="https://msdn.microsoft.com/cad38632-9f0a-4707-9086-b1248d6f31a6">IADsUser::SetPassword</a> in that it will use one of three methods to try to change the password. Initially, the LDAP provider will attempt an LDAP change password operation, if a secure SSL connection to the server is established.  If this attempt fails, the LDAP provider will next try to use Kerberos (see <b>IADsUser::SetPassword</b> for some problems that may result on  Windows with cross-forest authentication), and if this also fails, it will finally call the Active Directory specific network management API, <a href="https://msdn.microsoft.com/e3791756-3bd4-490b-983a-9687373d846b">NetUserChangePassword</a>.

In Active Directory, the caller must have the <a href="https://msdn.microsoft.com/15d2c52f-f626-4c6e-995d-19bbbbb38b6b">Change Password</a> extended control access right to change the password with this method.


#### Examples

The following code example shows how to change a user password.


```vb
Dim usr As IADsUser
Dim szOldPass As String
Dim szNewPass As String

On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith,user")
' Add code to securely retrieve the old and new password.

usr.ChangePassword szOldPass, szNewPass

Cleanup:
    If (Err.Number<>0) Then
        MsgBox("An error has occurred. " & Err.Number)
    End If
    Set usr = Nothing
```


The following code example shows how to change a user  password.


```cpp
HRESULT ChangePassword(
    IADsUser *pUser, 
    LPWSTR oldPasswd, 
    LPWSTR newPasswd)
{
    HRESULT hr=S_OK;
    if(!pUser) { return E_FAIL;}
    hr = pUser->ChangePassword(oldPasswd, newPasswd);
    printf("User password has been changed");
    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a>



<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IADsUser
  Property Methods</a>
 

 

