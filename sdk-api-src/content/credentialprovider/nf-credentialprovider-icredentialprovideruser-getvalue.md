---
UID: NF:credentialprovider.ICredentialProviderUser.GetValue
title: ICredentialProviderUser::GetValue (credentialprovider.h)
description: Retrieves a specified property value set for the user.
helpviewer_keywords: ["GetValue","GetValue method [Windows Shell]","GetValue method [Windows Shell]","ICredentialProviderUser interface","ICredentialProviderUser interface [Windows Shell]","GetValue method","ICredentialProviderUser.GetValue","ICredentialProviderUser::GetValue","credentialprovider/ICredentialProviderUser::GetValue","shell.ICredentialProviderUser_GetValue"]
old-location: shell\ICredentialProviderUser_GetValue.htm
tech.root: shell
ms.assetid: CA8CD897-127E-4113-A5A5-08110E0E6C17
ms.date: 12/05/2018
ms.keywords: GetValue, GetValue method [Windows Shell], GetValue method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetValue method, ICredentialProviderUser.GetValue, ICredentialProviderUser::GetValue, credentialprovider/ICredentialProviderUser::GetValue, shell.ICredentialProviderUser_GetValue
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
 - ICredentialProviderUser::GetValue
 - credentialprovider/ICredentialProviderUser::GetValue
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
 - ICredentialProviderUser.GetValue
---

# ICredentialProviderUser::GetValue


## -description

Retrieves a specified property value set for the user.

## -parameters

### -param key [in]

One of the following values that specify the property to retrieve.
                    
                        

<table class="clsStd">
<tr>
<th>REFPROPERTYKEY</th>
<th>Applies to...</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-displayname">PKEY_Identity_DisplayName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-username">PKEY_Identity_UserName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-qualifiedusername">PKEY_Identity_QualifiedUserName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-logonstatusstring">PKEY_Identity_LogonStatusString</a>
</td>
<td>Logon UI only</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-primarysid">PKEY_Identity_PrimarySid</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/properties/props-system-identity-providerid">PKEY_Identity_ProviderID</a>
</td>
<td>Logon and credential UI</td>
</tr>
</table>

### -param value [out]

A pointer to a value that, when this method returns successfully, receives the requested property value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The PKEY_Identity_DisplayName, PKEY_Identity_UserName, PKEY_Identity_QualifiedUserName, and PKEY_Identity_LogonStatusString values can be retrieved directly as strings through the <a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getstringvalue">GetStringValue</a> method.

## -see-also

<a href="/windows/desktop/api/credentialprovider/nn-credentialprovider-icredentialprovideruser">ICredentialProviderUser</a>



<a href="/windows/desktop/api/credentialprovider/nf-credentialprovider-icredentialprovideruser-getstringvalue">ICredentialProviderUser::GetStringValue</a>