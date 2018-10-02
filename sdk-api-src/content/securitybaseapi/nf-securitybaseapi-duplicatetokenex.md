---
UID: NF:securitybaseapi.DuplicateTokenEx
title: DuplicateTokenEx function
author: windows-sdk-content
description: Creates a new access token that duplicates an existing token. This function can create either a primary token or an impersonation token.
old-location: security\duplicatetokenex.htm
tech.root: SecAuthZ
ms.assetid: 96b13826-0ac7-4d70-9c21-eeb343f6b823
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DuplicateTokenEx, DuplicateTokenEx function [Security], TokenImpersonation, TokenPrimary, _win32_duplicatetokenex, security.duplicatetokenex, securitybaseapi/DuplicateTokenEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: securitybaseapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-Security-base-l1-1-0.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - DuplicateTokenEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DuplicateTokenEx function


## -description


The <b>DuplicateTokenEx</b> function creates a new <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> that duplicates an existing token. This function can create either a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> or an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


## -parameters




### -param hExistingToken [in]

A handle to an access token opened with TOKEN_DUPLICATE access.


### -param dwDesiredAccess [in]

Specifies the requested access rights for the new token. The <b>DuplicateTokenEx</b> function compares the requested access rights with the existing token's <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">discretionary access control list</a> (DACL) to determine which rights are granted or denied. To request the same access rights as the existing token, specify zero. To request all access rights that are valid for the caller, specify MAXIMUM_ALLOWED. 




For a list of access rights for access tokens, see 
<a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -param lpTokenAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security descriptor</a> for the new token and determines whether child processes can inherit the token. If <i>lpTokenAttributes</i> is <b>NULL</b>, the token gets a default security descriptor and the handle cannot be inherited. If the security descriptor contains a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">system access control list</a> (SACL), the token gets ACCESS_SYSTEM_SECURITY access right, even if it was not requested in <i>dwDesiredAccess</i>.

To set the owner in the security descriptor for the new token, the caller's process token must have the <b>SE_RESTORE_NAME</b> privilege set.


### -param ImpersonationLevel [in]

Specifies a value from the 
<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a> enumeration that indicates the impersonation level of the new token.


### -param TokenType [in]

Specifies one of the following values from the <a href="https://msdn.microsoft.com/51b6717e-3fda-4af4-8995-4ac571eae2fd">TOKEN_TYPE</a> enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TokenPrimary"></a><a id="tokenprimary"></a><a id="TOKENPRIMARY"></a><dl>
<dt><b>TokenPrimary</b></dt>
</dl>
</td>
<td width="60%">
The new token is a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> that you can use in the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="TokenImpersonation"></a><a id="tokenimpersonation"></a><a id="TOKENIMPERSONATION"></a><dl>
<dt><b>TokenImpersonation</b></dt>
</dl>
</td>
<td width="60%">
The new token is an impersonation token.

</td>
</tr>
</table>
 


### -param phNewToken [out]

A pointer to a <b>HANDLE</b> variable that receives the new token.

When you have finished using the new token, call the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function to close the token handle.


## -returns



If the function succeeds, the function returns a nonzero value.

If the function fails, it returns zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The <b>DuplicateTokenEx</b> function allows you to create a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> that you can use in the 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> function. This allows a server application that is impersonating a client to create a process that has the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> of the client. Note that the <a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a> function can create only impersonation tokens, which are not valid for <b>CreateProcessAsUser</b>.

The following is a typical scenario for using <b>DuplicateTokenEx</b> to create a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a>. A server application creates a thread that calls one of the impersonation functions, such as 
<a href="https://msdn.microsoft.com/63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b">ImpersonateNamedPipeClient</a>, to impersonate a client. The impersonating thread then calls the 
<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a> function to get its own token, which is an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a> that has the security context of the client. The thread specifies this impersonation token in a call to <b>DuplicateTokenEx</b>, specifying the TokenPrimary flag. The <b>DuplicateTokenEx</b> function creates a <i>primary token</i> that has the security context of the client.




## -see-also




<a href="https://msdn.microsoft.com/d9ce4ec5-5c09-4b33-93a1-39638a925986">Access Control</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375742(v=VS.85).aspx">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648756(v=VS.85).aspx">DdeImpersonateClient</a>



<a href="https://msdn.microsoft.com/796ec60e-fcae-48a9-b471-de3dce831306">DuplicateToken</a>



<a href="https://msdn.microsoft.com/63fc90ac-536a-4d9b-ba0d-19dc0cc09e6b">ImpersonateNamedPipeClient</a>



<a href="https://msdn.microsoft.com/5003f0c4-41e9-4a14-b6a9-4f259c4af08b">OpenThreadToken</a>



<a href="https://msdn.microsoft.com/e3de77b9-dd27-4f20-b63d-ad2c57ac4283">RevertToSelf</a>



<a href="https://msdn.microsoft.com/1b91c4dc-ac49-4002-b293-a25ca2ffcb21">RpcImpersonateClient</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/a75ad777-c88e-4899-be50-0118c113a600">SECURITY_IMPERSONATION_LEVEL</a>
 

 

