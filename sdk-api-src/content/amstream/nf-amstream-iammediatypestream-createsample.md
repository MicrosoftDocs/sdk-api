---
UID: NF:amstream.IAMMediaTypeStream.CreateSample
title: IAMMediaTypeStream::CreateSample
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The CreateSample method creates a stream sample and optionally specifies the sample buffer.
old-location: dshow\iammediatypestream_createsample.htm
tech.root: DirectShow
ms.assetid: 5bfdbf82-c298-498d-84e4-cd4d8cd13f82
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateSample, CreateSample method [DirectShow], CreateSample method [DirectShow],IAMMediaTypeStream interface, IAMMediaTypeStream interface [DirectShow],CreateSample method, IAMMediaTypeStream.CreateSample, IAMMediaTypeStream::CreateSample, IAMMediaTypeStreamCreateSample, amstream/IAMMediaTypeStream::CreateSample, dshow.iammediatypestream_createsample
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
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
 - amstream.h
api_name:
 - IAMMediaTypeStream.CreateSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeStream::CreateSample


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>CreateSample</code> method creates a stream sample and optionally specifies the sample buffer.




## -parameters




### -param lSampleSize [in]

Size of the sample.


### -param pbBuffer [in]

[optional] Pointer to an array of bytes that contains the sample data, or <b>NULL</b>.


### -param dwFlags [in]

Reserved.


### -param pUnkOuter [in]

[optional] Pointer to the interface of an object that aggregates the stream sample.


### -param ppAMMediaTypeSample [in]

Address of an <a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample</a> interface pointer that receives a pointer to the created sample.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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
</table>
 




## -remarks



If <i>pUnkOuter</i> is non-<b>NULL</b>, the new stream sample is aggregated into the specified object. Filters that receive the sample can then query it for interfaces supported by the aggregating object.




## -see-also




<a href="https://msdn.microsoft.com/6ca1bad2-625b-4415-8311-acd5443452c1">IAMMediaTypeStream Interface</a>
 

 

