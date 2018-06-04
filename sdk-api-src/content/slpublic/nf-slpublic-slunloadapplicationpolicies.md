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

# SLUnloadApplicationPolicies function


## -description


Releases the policy context handle returned by the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


## -parameters




### -param hPolicyContext [in]

Type: <b>HSLP</b>

The context handle returned by the <a href="https://msdn.microsoft.com/a0852c0c-3d7d-4cca-a30b-b413c653b284">SLLoadApplicationPolicies</a> function.


### -param dwFlags [in]

Type: <b>DWORD</b>

The additional flags.


## -returns



Type: <b>HRESULT WINAPI</b>

If this function succeeds, it return <b>S_OK</b>.  Otherwise, it returns an <b>HRESULT</b> error code.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
<dt>0x80070057</dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SL_E_APPLICATION_POLICIES_NOT_LOADED</b></dt>
<dt>0xC004F073</dt>
</dl>
</td>
<td width="60%">
The policy context was not found.

</td>
</tr>
</table>
 



