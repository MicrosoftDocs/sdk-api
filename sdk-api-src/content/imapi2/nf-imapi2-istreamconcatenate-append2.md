---
UID: NF:imapi2.IStreamConcatenate.Append2
title: IStreamConcatenate::Append2
author: windows-driver-content
description: Appends an array of streams to this stream.
old-location: imapi\istreamconcatenate_append2.htm
old-project: imapi
ms.assetid: 75e7f4cd-f3c8-494d-b049-7fe32c486659
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: Append2, Append2 method [IMAPI], Append2 method [IMAPI],IStreamConcatenate interface, IStreamConcatenate interface [IMAPI],Append2 method, IStreamConcatenate.Append2, IStreamConcatenate::Append2, imapi.istreamconcatenate_append2, imapi2/IStreamConcatenate::Append2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: IMAPI_READ_TRACK_ADDRESS_TYPE, *PIMAPI_READ_TRACK_ADDRESS_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	imapi2.h
api_name:
-	IStreamConcatenate.Append2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStreamConcatenate::Append2


## -description


Appends an array of streams to this stream.


## -parameters




### -param streams [in]

Array of  <b>IStream</b> interfaces of the streams to append to this stream.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -remarks



You must call the <a href="https://msdn.microsoft.com/62db148e-926d-47b3-a0f6-945730177184">IStreamConcatenate::Initialize</a> or <a href="https://msdn.microsoft.com/826b3157-4cab-4f18-87f2-6635911c03f0">IStreamConcatenate::Initialize2</a> method prior to calling this method.

To append a single stream to this stream, call the <a href="https://msdn.microsoft.com/9871cc35-c955-4fd4-9082-5b6ab60cae7b">IStreamConcatenate::Append</a> method.




## -see-also




<a href="https://msdn.microsoft.com/48b786ef-a1b6-4dcf-9329-c659f15185e1">IStreamConcatenate</a>



<a href="https://msdn.microsoft.com/9871cc35-c955-4fd4-9082-5b6ab60cae7b">IStreamConcatenate::Append</a>
 

 

