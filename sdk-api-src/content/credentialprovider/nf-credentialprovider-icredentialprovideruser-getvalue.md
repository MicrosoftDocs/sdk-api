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



The PKEY_Identity_DisplayName, PKEY_Identity_UserName, PKEY_Identity_QualifiedUserName, and PKEY_Identity_LogonStatusString values can be retrieved directly as strings through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597621">GetStringValue</a> method.




## -see-also




<a href="https://msdn.microsoft.com/8EE5FA54-E20E-4d24-AD73-2AE1F0090950">ICredentialProviderUser</a>



<a href="https://msdn.microsoft.com/97FFD00F-6141-472c-A60C-A9A282190C9D">ICredentialProviderUser::GetStringValue</a>
 

 

