---
UID: NF:imapi2.IStreamInterleave.Initialize
title: IStreamInterleave::Initialize
author: windows-sdk-content
description: Initialize this interleaved stream from an array of input streams and interleave sizes.
old-location: imapi\istreaminterleave_initialize.htm
old-project: imapi
ms.assetid: 889db097-3a16-4c35-9a79-e4a9d8060832
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: IStreamInterleave interface [IMAPI],Initialize method, IStreamInterleave.Initialize, IStreamInterleave::Initialize, Initialize, Initialize method [IMAPI], Initialize method [IMAPI],IStreamInterleave interface, imapi.istreaminterleave_initialize, imapi2/IStreamInterleave::Initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamInterleave.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamInterleave::Initialize


## -description


Initialize this interleaved stream from an array of input streams and interleave sizes.


## -parameters




### -param streams [in]

Array of  <b>IStream</b> interfaces of the streams to add to this stream.


### -param interleaveSizes [in]

Array of interleave sizes, in bytes, with one entry per stream. The interleave size array is the number of contiguous bytes of a given stream to write on the disc before writing starts for the next stream.


### -param streamCount [in]

Number of streams in <i>streams</i>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Failed to allocate the required memory.

Value: 0x8007000E

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

Value: 0x80070057

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2d0f03e5-a47d-4b46-a177-f462bbafe153">IStreamInterleave</a>
 

 

