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

# IMFDRMNetHelper::ProcessLicenseRequest


## -description


Gets the license response for the specified request.


## -parameters




### -param pLicenseRequest [in]

Pointer to a byte array that contains the license request.


### -param cbLicenseRequest [in]

Size, in bytes, of the license request.


### -param ppLicenseResponse [out]

Receives a pointer to a byte array that contains the license response. The caller must free the array by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.


### -param pcbLicenseResponse [out]

Receives the size, in bytes, of the license response.


### -param pbstrKID [out]

Receives the key identifier. The caller must release the string by calling <b>SysFreeString</b>.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media sink was shut down.


</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f4ac19a-0972-4152-a64c-6c719efb396c">IMFDRMNetHelper</a>
 

 

