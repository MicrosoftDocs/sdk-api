---
UID: NF:credentialprovider.ICredentialProviderUser.GetStringValue
title: ICredentialProviderUser::GetStringValue
author: windows-sdk-content
description: Retrieves string properties from the ICredentialProviderUser object based on the input value.
old-location: shell\ICredentialProviderUser_GetStringValue.htm
tech.root: shell
ms.assetid: 97FFD00F-6141-472c-A60C-A9A282190C9D
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetStringValue, GetStringValue method [Windows Shell], GetStringValue method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetStringValue method, ICredentialProviderUser.GetStringValue, ICredentialProviderUser::GetStringValue, credentialprovider/ICredentialProviderUser::GetStringValue, shell.ICredentialProviderUser_GetStringValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: credentialprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: CredentialProvider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CredentialProvider.lib
req.dll: Authui.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUser.GetStringValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICredentialProviderUser::GetStringValue


## -description


Retrieves string properties from the <a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a> object based on the input value.


## -parameters




### -param key [in]

One of the following values that specify the property to retrieve.
                    
                        

<table>
<tr>
<th>REFPROPERTYKEY</th>
<th>Description</th>
<th>Applies to...</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/17bf848f-6d45-4588-aaa7-50fe99579440">PKEY_Identity_DisplayName</a>
</td>
<td>The friendly user name.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8B12E452-790D-4924-98E7-9368CC525674">PKEY_Identity_LogonStatusString</a>
</td>
<td>A localized string that indicates the user's logged on status.</td>
<td>Logon UI only</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/F4808C32-2C07-4B88-B672-300AA3BFD162">PKEY_Identity_PrimarySid</a>
</td>
<td>The user's SID.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/837ba603-76dc-442d-ba4a-0f87ac116dfd">PKEY_Identity_ProviderID</a>
</td>
<td>The user's provider ID.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08AC11E1-1C0B-4D8A-94B0-F1EDA1B02F43">PKEY_Identity_QualifiedUserName</a>
</td>
<td>The name used to pack an authentication buffer.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/da13b18d-0450-49fd-8c10-08413d55587e">PKEY_Identity_UserName</a>
</td>
<td>The user name.</td>
<td>Logon UI and Credential UI</td>
</tr>
</table>
 


### -param stringValue [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the requested string.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each of these values can also be retrieved as a <b>PROPVARIANT</b> through <a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>.

Consider a scenario with the following users.

<ul>
<li>Domain user:<ul>
<li>Domain: contoso</li>
<li>User name: lisa</li>
<li>Friendly name: Lisa Andrews</li>
</ul>
</li>
<li>Local user:<ul>
<li>PC name: lisa-pc</li>
<li>User name: lisa</li>
<li>Friendly name: Lisa Andrews</li>
</ul>
</li>
<li>Microsoft account:<ul>
<li>Email address: lisa@contoso.com</li>
<li>Friendly name: Lisa Andrews</li>
</ul>
</li>
</ul>
In this scenario, the following table provides some sample data for each of the <i>key</i> values.

<table>
<tr>
<th>REFPROPERTYKEY</th>
<th>Domain user</th>
<th>Local user</th>
<th>Microsoft account</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/17bf848f-6d45-4588-aaa7-50fe99579440">PKEY_Identity_DisplayName</a>
</td>
<td>"Lisa Andrews"</td>
<td>"Lisa Andrews"</td>
<td>"Lisa Andrews"</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8B12E452-790D-4924-98E7-9368CC525674">PKEY_Identity_LogonStatusString</a>
</td>
<td>"Signed-in"</td>
<td>"Locked"</td>
<td>"Remotely signed in from lisa-pc"</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/F4808C32-2C07-4B88-B672-300AA3BFD162">PKEY_Identity_PrimarySid</a>
</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/837ba603-76dc-442d-ba4a-0f87ac116dfd">PKEY_Identity_ProviderID</a>
</td>
<td>"{A198529B-730F-4089-B646-A12557F5665E}"</td>
<td>"{A198529B-730F-4089-B646-A12557F5665E}"</td>
<td>Not pre-defined</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08AC11E1-1C0B-4D8A-94B0-F1EDA1B02F43">PKEY_Identity_QualifiedUserName</a>
</td>
<td>"contoso\lisa"</td>
<td>"lisa-pc\lisa"</td>
<td>"&lt;account provider name&gt;\lisa@contoso.com"</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/da13b18d-0450-49fd-8c10-08413d55587e">PKEY_Identity_UserName</a>
</td>
<td>"contoso\lisa"</td>
<td>"lisa"</td>
<td>"lisa@contoso.com"</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/CA8CD897-127E-4113-A5A5-08110E0E6C17">ICredentialProviderUser::GetValue</a>
 

 

