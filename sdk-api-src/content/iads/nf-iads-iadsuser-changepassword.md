---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim usr As IADsUser
Dim szOldPass As String
Dim szNewPass As String

On Error GoTo Cleanup

Set usr = GetObject("WinNT://Fabrikam/JeffSmith,user")
' Add code to securely retrieve the old and new password.

usr.ChangePassword szOldPass, szNewPass

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set usr = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to change a user  password.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT ChangePassword(
    IADsUser *pUser, 
    LPWSTR oldPasswd, 
    LPWSTR newPasswd)
{
    HRESULT hr=S_OK;
    if(!pUser) { return E_FAIL;}
    hr = pUser-&gt;ChangePassword(oldPasswd, newPasswd);
    printf("User password has been changed");
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/6eea74c2-2d6d-4dfd-9a22-3da2d5ce49bf">IADsUser</a>



<a href="https://msdn.microsoft.com/02d0e5f1-8bc9-4ef6-962d-432654ca8433">IADsUser
  Property Methods</a>
 

 

