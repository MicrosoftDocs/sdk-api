---
UID: NF:mmstream.IMultiMediaStream.GetDuration
title: IMultiMediaStream::GetDuration
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The GetDuration method retrieves the duration of the multimedia stream.
old-location: dshow\imultimediastream_getduration.htm
tech.root: DirectShow
ms.assetid: 4d8104ec-aa2a-4151-bb7f-53611d4a71f2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetDuration, GetDuration method [DirectShow], GetDuration method [DirectShow],IMultiMediaStream interface, IMultiMediaStream interface [DirectShow],GetDuration method, IMultiMediaStream.GetDuration, IMultiMediaStream::GetDuration, IMultiMediaStreamGetDuration, dshow.imultimediastream_getduration, mmstream/IMultiMediaStream::GetDuration
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmstream.h
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
 - mmstream.h
api_name:
 - IMultiMediaStream.GetDuration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMultiMediaStream::GetDuration


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>GetDuration</code> method retrieves the duration of the multimedia stream.




## -parameters




### -param pDuration [out]

Pointer to a variable that receives of the multimedia stream, in 100-nanosecond units.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
This multimedia stream does not support seeking.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MS_E_INVALIDSTREAMTYPE</b></dt>
</dl>
</td>
<td width="60%">
This multimedia stream is not read-only.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Could not determine the duration.

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
 




## -see-also




<a href="https://msdn.microsoft.com/8be6c74f-9290-48b4-ad66-8d7d7cc94174">IMultiMediaStream Interface</a>
 

 

