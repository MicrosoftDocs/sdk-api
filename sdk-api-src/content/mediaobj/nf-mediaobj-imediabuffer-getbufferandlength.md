---
UID: NF:mediaobj.IMediaBuffer.GetBufferAndLength
title: IMediaBuffer::GetBufferAndLength (mediaobj.h)
description: The GetBufferAndLength method retrieves the buffer and the size of the valid data in the buffer.helpviewer_keywords: ["GetBufferAndLength","GetBufferAndLength method [DirectShow]","GetBufferAndLength method [DirectShow]","IMediaBuffer interface","IMediaBuffer interface [DirectShow]","GetBufferAndLength method","IMediaBuffer.GetBufferAndLength","IMediaBuffer::GetBufferAndLength","IMediaBufferGetBufferAndLength","dshow.imediabuffer_getbufferandlength","mediaobj/IMediaBuffer::GetBufferAndLength"]
old-location: dshow\imediabuffer_getbufferandlength.htm
tech.root: DirectShow
ms.assetid: 255ef101-f004-41c8-afb8-437d21decee5
ms.date: 12/05/2018
ms.keywords: GetBufferAndLength, GetBufferAndLength method [DirectShow], GetBufferAndLength method [DirectShow],IMediaBuffer interface, IMediaBuffer interface [DirectShow],GetBufferAndLength method, IMediaBuffer.GetBufferAndLength, IMediaBuffer::GetBufferAndLength, IMediaBufferGetBufferAndLength, dshow.imediabuffer_getbufferandlength, mediaobj/IMediaBuffer::GetBufferAndLength
f1_keywords:
- mediaobj/IMediaBuffer.GetBufferAndLength
dev_langs:
- c++
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dmoguids.lib
- Dmoguids.dll
api_name:
- IMediaBuffer.GetBufferAndLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMediaBuffer::GetBufferAndLength


## -description



The <code>GetBufferAndLength</code> method retrieves the buffer and the size of the valid data in the buffer.




## -parameters




### -param ppBuffer [out]

Address of a pointer that receives the buffer array. Can be <b>NULL</b> if <i>pcbLength</i> is not <b>NULL</b>.


### -param pcbLength [out]

Pointer to a variable that receives the size of the valid data, in bytes. Can be <b>NULL</b> if <i>ppBuffer</i> is not <b>NULL</b>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

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
 




## -remarks



Either parameter can be <b>NULL</b>, in which case it does not receive a value. At least one parameter must be non-<b>NULL</b>. If both parameters are <b>NULL</b>, the method returns E_POINTER.

The value returned in the <i>pcbLength</i> parameter is the size of the valid data in the buffer, not the buffer's allocated size. To obtain the buffer's allocated size, call the <a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nf-mediaobj-imediabuffer-getmaxlength">IMediaBuffer::GetMaxLength</a> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer">IMediaBuffer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/implementing-imediabuffer">Implementing IMediaBuffer</a>
 

 

