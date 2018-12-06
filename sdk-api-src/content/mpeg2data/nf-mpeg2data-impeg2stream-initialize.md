---
UID: NF:mpeg2data.IMpeg2Stream.Initialize
title: IMpeg2Stream::Initialize
author: windows-sdk-content
description: The Initialize method initializes the MPEG2Stream object. This method should be called once, immediately after creating the object. The IMpeg2Data::GetStreamOfSections method calls this method internally, so typically an application will not call it.
old-location: mstv\impeg2stream_initialize.htm
tech.root: mstv
ms.assetid: a2ef2ebc-55dc-49d4-a5de-18203de113ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IMpeg2Stream interface [Microsoft TV Technologies],Initialize method, IMpeg2Stream.Initialize, IMpeg2Stream::Initialize, IMpeg2StreamInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IMpeg2Stream interface, mpeg2data/IMpeg2Stream::Initialize, mstv.impeg2stream_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mpeg2data.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - IMpeg2Stream.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2Stream::Initialize


## -description



The <b>Initialize</b> method initializes the <b>MPEG2Stream</b> object. This method should be called once, immediately after creating the object. The <a href="https://msdn.microsoft.com/896080ff-cdf0-40b1-ba4e-d94de527d86e">IMpeg2Data::GetStreamOfSections</a> method calls this method internally, so typically an application will not call it.




## -parameters




### -param requestType [in]

Specifies the request type, as an <a href="https://msdn.microsoft.com/d1811cd5-3dda-48d1-a3b3-e4189e2622bb">MPEG_REQUEST_TYPE</a> value.


### -param pMpeg2Data [in]

Pointer to the <a href="https://msdn.microsoft.com/82af47a2-cac4-4d4f-ba20-d4f6b5485a65">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


### -param pContext [in]

Pointer to an <a href="https://msdn.microsoft.com/7a92e545-805b-4ce6-bbf1-397f7a5f6524">MPEG_CONTEXT</a> structure. This structure indicates the MPEG-2 source.


### -param pid [in]

Specifies a packet identifier (PID), indicating which packets in the transport stream are requested.


### -param tid [in]

Specifies a table identifier (TID), indicating which table sections to retrieve.


### -param pFilter [in]

Optional pointer to an <a href="https://msdn.microsoft.com/a7e66de7-d67b-4814-9849-076c3dd5afb1">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.


### -param hDataReadyEvent [in]

Handle to an event. The filter signals this event whenever it receives new data.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid or <b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The method has been called on this object already.

</td>
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/189c921a-ec49-48dc-8c60-3d3ec2a648ca">IMpeg2Stream Interface</a>
 

 

