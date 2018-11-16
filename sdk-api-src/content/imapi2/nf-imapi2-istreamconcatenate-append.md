---
UID: NF:imapi2.IStreamConcatenate.Append
title: IStreamConcatenate::Append
author: windows-sdk-content
description: Appends a stream to this stream.
old-location: imapi\istreamconcatenate_append.htm
tech.root: imapi
ms.assetid: 9871cc35-c955-4fd4-9082-5b6ab60cae7b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Append, Append method [IMAPI], Append method [IMAPI],IStreamConcatenate interface, IStreamConcatenate interface [IMAPI],Append method, IStreamConcatenate.Append, IStreamConcatenate::Append, imapi.istreamconcatenate_append, imapi2/IStreamConcatenate::Append
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IStreamConcatenate.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- imapi2.h
: 
- IStreamConcatenate.Append
: 
---

# IStreamConcatenate::Append


## -description


Appends a stream to this stream.


## -parameters




### -param stream [in]

An <b>IStream</b> interface of the stream to append to this stream.


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

To append more than one stream to this stream, call the <a href="https://msdn.microsoft.com/75e7f4cd-f3c8-494d-b049-7fe32c486659">IStreamConcatenate::Append2</a> method.




## -see-also




<a href="https://msdn.microsoft.com/48b786ef-a1b6-4dcf-9329-c659f15185e1">IStreamConcatenate</a>



<a href="https://msdn.microsoft.com/75e7f4cd-f3c8-494d-b049-7fe32c486659">IStreamConcatenate::Append2</a>
 

 

