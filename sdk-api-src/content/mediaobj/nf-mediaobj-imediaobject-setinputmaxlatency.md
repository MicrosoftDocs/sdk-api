---
UID: NF:mediaobj.IMediaObject.SetInputMaxLatency
title: IMediaObject::SetInputMaxLatency
author: windows-sdk-content
description: The SetInputMaxLatency method sets the maximum latency on a specified input stream. For the definition of maximum latency, see IMediaObject::GetInputMaxLatency.
old-location: dshow\imediaobject_setinputmaxlatency.htm
old-project: DirectShow
ms.assetid: 45fb0caa-cd12-4847-a646-f6fd90c50b81
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMediaObject interface [DirectShow],SetInputMaxLatency method, IMediaObject.SetInputMaxLatency, IMediaObject::SetInputMaxLatency, IMediaObjectSetInputMaxLatency, SetInputMaxLatency, SetInputMaxLatency method [DirectShow], SetInputMaxLatency method [DirectShow],IMediaObject interface, dshow.imediaobject_setinputmaxlatency, mediaobj/IMediaObject::SetInputMaxLatency
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mediaobj.h
req.include-header: Dmo.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObject.SetInputMaxLatency
product: Windows
targetos: Windows
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMediaObject::SetInputMaxLatency


## -description



The <code>SetInputMaxLatency</code> method sets the maximum latency on a specified input stream. For the definition of maximum latency, see <a href="https://msdn.microsoft.com/f8a18b4c-a59c-4e9d-aff7-62333e9ffda9">IMediaObject::GetInputMaxLatency</a>.




## -parameters




### -param dwInputStreamIndex

Zero-based index of an input stream on the DMO.


### -param rtMaxLatency

Maximum latency.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMO_E_INVALIDSTREAMINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream index

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a3fd17aa-7df2-40f4-8f2c-45bae38e4c0b">IMediaObject Interface</a>



<a href="https://msdn.microsoft.com/f8a18b4c-a59c-4e9d-aff7-62333e9ffda9">IMediaObject::GetInputMaxLatency</a>
 

 

