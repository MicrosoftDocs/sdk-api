---
UID: NF:credentialprovider.ICredentialProviderUser.GetValue
title: ICredentialProviderUser::GetValue
author: windows-sdk-content
description: Retrieves a specified property value set for the user.
old-location: shell\ICredentialProviderUser_GetValue.htm
tech.root: shell
ms.assetid: CA8CD897-127E-4113-A5A5-08110E0E6C17
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: GetValue, GetValue method [Windows Shell], GetValue method [Windows Shell],ICredentialProviderUser interface, ICredentialProviderUser interface [Windows Shell],GetValue method, ICredentialProviderUser.GetValue, ICredentialProviderUser::GetValue, credentialprovider/ICredentialProviderUser::GetValue, shell.ICredentialProviderUser_GetValue
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
 - ICredentialProviderUser.GetValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/17bf848f-6d45-4588-aaa7-50fe99579440">PKEY_Identity_DisplayName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/da13b18d-0450-49fd-8c10-08413d55587e">PKEY_Identity_UserName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08AC11E1-1C0B-4D8A-94B0-F1EDA1B02F43">PKEY_Identity_QualifiedUserName</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8B12E452-790D-4924-98E7-9368CC525674">PKEY_Identity_LogonStatusString</a>
</td>
<td>Logon UI only</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/F4808C32-2C07-4B88-B672-300AA3BFD162">PKEY_Identity_PrimarySid</a>
</td>
<td>Logon and credential UI</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/837ba603-76dc-442d-ba4a-0f87ac116dfd">PKEY_Identity_ProviderID</a>
</td>
<td>Logon and credential UI</td>
</tr>
</table>
 


### -param value [out]

A pointer to a value that, when this method returns successfully, receives the requested property value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The PKEY_Identity_DisplayName, PKEY_Identity_UserName, PKEY_Identity_QualifiedUserName, and PKEY_Identity_LogonStatusString values can be retrieved directly as strings through the <a href="https://msdn.microsoft.com/97FFD00F-6141-472c-A60C-A9A282190C9D">GetStringValue</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/97FFD00F-6141-472c-A60C-A9A282190C9D">ICredentialProviderUser::GetStringValue</a>
 

 

