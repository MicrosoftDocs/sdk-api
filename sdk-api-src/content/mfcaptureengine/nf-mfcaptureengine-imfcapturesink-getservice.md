---
UID: NF:mfcaptureengine.IMFCaptureSink.GetService
title: IMFCaptureSink::GetService
author: windows-driver-content
description: Queries the underlying Sink Writer object for an interface.
old-location: mf\imfcapturesink_getservice.htm
old-project: medfound
ms.assetid: 591F0E3D-01A8-420F-86C6-2C610643EB69
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: GetService, GetService method [Media Foundation], GetService method [Media Foundation],IMFCaptureSink interface, IMFCaptureSink interface [Media Foundation],GetService method, IMFCaptureSink.GetService, IMFCaptureSink::GetService, mf.imfcapturesink_getservice, mfcaptureengine/IMFCaptureSink::GetService
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
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureSink.GetService
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureSink::GetService


## -description


Queries the underlying <a href="https://msdn.microsoft.com/23AF25B8-B94C-48BC-83D8-5863ACFFD4CA">Sink Writer</a> object for an interface.


## -parameters




### -param dwSinkStreamIndex [in]

The zero-based index of the stream to query. The index is returned in the <i>pdwSinkStreamIndex</i> parameter of the <a href="https://msdn.microsoft.com/5D7A1FE0-92B9-4CC4-A268-17FA848055A9">IMFCaptureSink::AddStream</a> method.


### -param rguidService [in]

A service identifier GUID. Currently, the value must be <b>GUID_NULL</b>.


### -param riid [in]

A service identifier GUID. Currently, the value must be <b>IID_IMFSinkWriter</b>.


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
Invalid request.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>
 

 

