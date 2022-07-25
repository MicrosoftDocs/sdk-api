---
UID: NF:credentialprovider.ICredentialProviderUser.GetStringValue
title: ICredentialProviderUser::GetStringValue (credentialprovider.h)
description: Retrieves string properties from the ICredentialProviderUser object based on the input value.
helpviewer_keywords: ["GetStringValue","GetStringValue method [Windows Shell]","GetStringValue method [Windows Shell]","ICredentialProviderUser interface","ICredentialProviderUser interface [Windows Shell]","GetStringValue method","ICredentialProviderUser.GetStringValue","ICredentialProviderUser::GetStringValue","credentialprovider/ICredentialProviderUser::GetStringValue","shell.ICredentialProviderUser_GetStringValue"]
old-location: shell\ICredentialProviderUser_GetStringValue.htm
tech.root: shell
ms.assetid: 97FFD00F-6141-472c-A60C-A9A282190C9D
ms.date: 12/05/2018
ms.keywords: GetStringValue, GetStringValue method [Windows Shell], GetStringValue method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetStringValue method, ICredentialProviderUser.GetStringValue, ICredentialProviderUser::GetStringValue, credentialprovider/ICredentialProviderUser::GetStringValue, shell.ICredentialProviderUser_GetStringValue
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICredentialProviderUser::GetStringValue
 - credentialprovider/ICredentialProviderUser::GetStringValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Authui.dll
api_name:
 - ICredentialProviderUser.GetStringValue
---

# ICredentialProviderUser::GetStringValue


## -description

Retrieves string properties from the <a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a> object based on the input value.

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
<a href="/windows/desktop/properties/props-system-identity-displayname">PKEY_Identity_DisplayName</a>
</td>
<td>The friendly user name.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-logonstatusstring">PKEY_Identity_LogonStatusString</a>
</td>
<td>A localized string that indicates the user's logged on status.</td>
<td>Logon UI only</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-primarysid">PKEY_Identity_PrimarySid</a>
</td>
<td>The user's SID.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-providerid">PKEY_Identity_ProviderID</a>
</td>
<td>The user's provider ID.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-qualifiedusername">PKEY_Identity_QualifiedUserName</a>
</td>
<td>The name used to pack an authentication buffer.</td>
<td>Logon UI and Credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-username">PKEY_Identity_UserName</a>
</td>
<td>The user name.</td>
<td>Logon UI and Credential UI</td>
</tr>
</table>

### -param stringValue [out]

The address of a pointer to a buffer that, when this method returns successfully, receives the requested string.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each of these values can also be retrieved as a <b>PROPVARIANT</b> through <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>.

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
<a href="/windows/desktop/properties/props-system-identity-displayname">PKEY_Identity_DisplayName</a>
</td>
<td>"Lisa Andrews"</td>
<td>"Lisa Andrews"</td>
<td>"Lisa Andrews"</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-logonstatusstring">PKEY_Identity_LogonStatusString</a>
</td>
<td>"Signed-in"</td>
<td>"Locked"</td>
<td>"Remotely signed in from lisa-pc"</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-primarysid">PKEY_Identity_PrimarySid</a>
</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
<td>"{S-1-5-21-2279990834-2601404236-735077814-1001}"</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-providerid">PKEY_Identity_ProviderID</a>
</td>
<td>"{A198529B-730F-4089-B646-A12557F5665E}"</td>
<td>"{A198529B-730F-4089-B646-A12557F5665E}"</td>
<td>Not pre-defined</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-qualifiedusername">PKEY_Identity_QualifiedUserName</a>
</td>
<td>"contoso\lisa"</td>
<td>"lisa-pc\lisa"</td>
<td>"&lt;account provider name&gt;\lisa@contoso.com"</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-username">PKEY_Identity_UserName</a>
</td>
<td>"contoso\lisa"</td>
<td>"lisa"</td>
<td>"lisa@contoso.com"</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getvalue">ICredentialProviderUser::GetValue</a>