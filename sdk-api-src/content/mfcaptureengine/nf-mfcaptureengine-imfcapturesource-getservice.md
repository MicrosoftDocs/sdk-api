---
UID: NF:mfcaptureengine.IMFCaptureSource.GetService
title: IMFCaptureSource::GetService
author: windows-sdk-content
description: Gets a pointer to the underlying Source Reader object.
old-location: mf\imfcapturesource_getservice.htm
tech.root: MedFound
ms.assetid: 67A77196-A499-4C28-8A35-CFB130B85D79
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetService, GetService method [Media Foundation], GetService method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetService method, IMFCaptureSource.GetService, IMFCaptureSource::GetService, mf.imfcapturesource_getservice, mfcaptureengine/IMFCaptureSource::GetService
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - mfcaptureengine.h
api_name:
 - IMFCaptureSource.GetService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetService


## -description


Gets a pointer to the underlying <a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a> object.


## -parameters




### -param rguidService [in]

A service identifier GUID. Currently the value must be <b>IID_IMFSourceReader</b> or <b>GUID_NULL</b>.


### -param riid [in]

The interface identifier (IID) of the interface being requested. The value must be <b>IID_IMFSourceReader</b>. If the value is not set to <b>IID_IMFSourceReader</b>, the call  will fail and return <b>E_INVALIDARG</b>.


### -param ppUnknown [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. The caller must release the interface.




## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The capture source was not initialized. Possibly there is no capture device on the system.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

