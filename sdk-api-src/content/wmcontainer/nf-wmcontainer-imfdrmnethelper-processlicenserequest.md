---
UID: NF:wmcontainer.IMFDRMNetHelper.ProcessLicenseRequest
title: IMFDRMNetHelper::ProcessLicenseRequest
author: windows-sdk-content
description: Gets the license response for the specified request.
old-location: mf\imfdrmnethelper_processlicenserequest.htm
tech.root: medfound
ms.assetid: e60f9831-f59d-46ff-b685-b26d6484a70d
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IMFDRMNetHelper interface [Media Foundation],ProcessLicenseRequest method, IMFDRMNetHelper.ProcessLicenseRequest, IMFDRMNetHelper::ProcessLicenseRequest, ProcessLicenseRequest, ProcessLicenseRequest method [Media Foundation], ProcessLicenseRequest method [Media Foundation],IMFDRMNetHelper interface, mf.imfdrmnethelper_processlicenserequest, wmcontainer/IMFDRMNetHelper::ProcessLicenseRequest
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmcontainer.h
api_name:
 - IMFDRMNetHelper.ProcessLicenseRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

