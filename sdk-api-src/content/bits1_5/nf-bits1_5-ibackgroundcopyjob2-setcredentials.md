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

# IBackgroundCopyJob2::SetCredentials


## -description



			Specifies the credentials to use for a proxy or remote server user authentication request.


## -parameters




### -param credentials






#### - Credentials [in]

Identifies the target (proxy or server), authentication scheme, and the user's credentials to use for user authentication. For details, see the 
<a href="https://msdn.microsoft.com/f89ebf46-da83-495c-bafe-b2e0f72f5d8e">BG_AUTH_CREDENTIALS</a> structure.


## -returns



This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_AUTH_TARGET</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized target enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_INVALID_AUTH_SCHEME</b></dt>
</dl>
</td>
<td width="60%">
Unrecognized scheme enumeration value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_USERNAME_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The user name is too long. For the limit, see the <a href="https://msdn.microsoft.com/e078e464-37b7-45ce-add8-6472a4607ff3">BG_BASIC_CREDENTIALS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>BG_E_PASSWORD_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The password is too long. For the limit, see the <a href="https://msdn.microsoft.com/e078e464-37b7-45ce-add8-6472a4607ff3">BG_BASIC_CREDENTIALS</a> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The UserName and Password members of the <a href="https://msdn.microsoft.com/e078e464-37b7-45ce-add8-6472a4607ff3">BG_BASIC_CREDENTIALS</a> structure cannot be <b>NULL</b> if you specify the Basic or Digest scheme.

</td>
</tr>
</table>
 




## -remarks



 BITS provides the credentials to a proxy or server in response to a request for user authentication. Set the credentials before the initial call to <a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">Resume</a>. 

You must call this method for each target and scheme pair that you want to provide. For example, if you want to specify proxy credentials for both Basic and Digest authentication, you would call this method once to specify the Basic credentials and a second time to specify the Digest credentials.

If the job currently contains credentials with the same target and scheme pair, the existing credentials are replaced with the new credentials. The credentials persist for the life of the job. To remove the credentials from the job, call the 
<a href="https://msdn.microsoft.com/dbc6a05d-9e1f-4cc9-b28b-0874aafdfd7c">IBackgroundCopyJob2::RemoveCredentials</a> method.

If you know the schemes the proxy or server will request, you can provide only those credentials. Otherwise, provide credentials for all schemes. 

The job enters the <b>BG_JOB_STATE_ERROR</b> state if you do not provide the credentials requested by the proxy or server, or the proxy or server cannot authenticate the credentials. Check the error code to determine if the authentication failed at the server (<b>BG_E_HTTP_ERROR_401</b>) or proxy (<b>BG_E_HTTP_ERROR_407</b>). To retrieve the error code, call the 
<a href="https://msdn.microsoft.com/2ad4c913-2d1e-4490-968c-960178a57e3b">IBackgroundCopyJob::GetError</a> method to retrieve an 
<a href="https://msdn.microsoft.com/a0b9e887-84d5-4f67-a65c-6a807c50dafd">IBackgroundCopyError</a> interface pointer. Then, call the 
<a href="https://msdn.microsoft.com/abdf115d-3ff2-4664-b053-f55872ad24ab">IBackgroundCopyError::GetError</a> method to retrieve the error code. After you determine where the authentication failed (proxy or server), specify new credentials to use for the proxy or server and call the 
<a href="https://msdn.microsoft.com/a9e6f057-0a51-4f2d-810b-edbb3e019370">IBackgroundCopyJob::Resume</a> method to resume the job. Because you cannot determine which scheme failed, specify credentials for all schemes before calling the 
<b>Resume</b> method.

There is no method to retrieve credentials that you have set.

You must call this method in the context of the job's owner.

Calling the 
<a href="https://msdn.microsoft.com/12ac2dd8-516b-4b5d-a2bf-0abb55d18ee0">IBackgroundCopyJob::TakeOwnership</a> method removes the credentials from the job.

To specify implicit credentials (the logged on user's credentials), set the scheme to NTLM and the user name and password to <b>NULL</b>. If you specify implicit credentials for a proxy, BITS will also use the implicit credentials for server authentication unless you specify explicit server credentials. 

<div class="alert"><b>Note</b>  BITS ignores credentials for <a href="https://msdn.microsoft.com/bf5302e9-da8f-4c57-a998-fd49484e0584">remote names</a> that specify an SMB path.</div>
<div> </div>
<div class="alert"><b>Note</b>  BITS does not authenticate the server or encrypt the channel. Use HTTPS if this is an issue for your application.</div>
<div> </div>

#### Examples

The following example shows how to call the 
<b>SetCredentials</b> method to specify Basic credentials for a server user authentication request. The example uses the 
<a href="https://msdn.microsoft.com/97a8e750-3e63-4e6f-a875-1e5c49c30dd4">CredUIPromptForCredentials</a> function to capture the user name and password. The example assumes a valid 
<a href="https://msdn.microsoft.com/91dd1ae1-1740-4d95-a476-fc18aead1dc2">IBackgroundCopyJob</a> interface pointer, pJob. The example uses the <a href="https://msdn.microsoft.com/2c4090a6-025b-4b7b-8f31-7e744ad51b39">SecureZeroMemory</a> function to clear the memory locations associated with the sensitive information. The <b>SecureZeroMemory</b> function is defined in WinBase.h.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define MAX_STR_LENGTH 300+1    // BITS limit for user name and password

CREDUI_INFO cuiinfo;
WCHAR szUserName[MAX_STR_LENGTH];  
WCHAR szPassword[MAX_STR_LENGTH];
DWORD rc;
IBackgroundCopyJob* pJob;
IBackgroundCopyJob2* pJob2 = NULL;
BG_AUTH_CREDENTIALS ac;

cuiinfo.cbSize = sizeof(CREDUI_INFO);
cuiinfo.hbmBanner = NULL;
cuiinfo.hwndParent = NULL; //Desktop is parent
cuiinfo.pszCaptionText = L"Server Authentication";
cuiinfo.pszMessageText = L"Enter user credentials for Basic authentication.";

//Initialize the UserName and Password fields. This example sets  
//UserName to blank, but you could also set UserName to the owner 
//of the job or the current user. For an example that retrieves the owner's
//name, see the example code for the IBackgroundCopyJob::GetOwner method. 
szUserName[0] = L'\0';
szPassword[0] = L'\0';
rc = CredUIPromptForCredentials(&amp;cuiinfo, NULL, NULL, 0,
    szUserName, MAX_STR_LENGTH,
    szPassword, MAX_STR_LENGTH, 
    NULL, CREDUI_FLAGS_DO_NOT_PERSIST | CREDUI_FLAGS_GENERIC_CREDENTIALS);

if (NO_ERROR == rc)
{
    pJob-&gt;QueryInterface(__uuidof(IBackgroundCopyJob2), (void**)&amp;pJob2);
    ac.Target = BG_AUTH_TARGET_SERVER;
    ac.Scheme = BG_AUTH_SCHEME_BASIC;
    ac.Credentials.Basic.UserName = szUserName;
    ac.Credentials.Basic.Password = szPassword;
    hr = pJob2-&gt;SetCredentials(&amp;ac);
    if (FAILED(hr))
    {
      //Handle error
    }
    SecureZeroMemory(szUserName, sizeof(szUserName));
    SecureZeroMemory(szPassword, sizeof(szPassword));
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt427474">Authentication</a>



<a href="https://msdn.microsoft.com/f89ebf46-da83-495c-bafe-b2e0f72f5d8e">BG_AUTH_CREDENTIALS</a>



<a href="https://msdn.microsoft.com/dbc6a05d-9e1f-4cc9-b28b-0874aafdfd7c">IBackgroundCopyJob2::RemoveCredentials</a>
 

 

