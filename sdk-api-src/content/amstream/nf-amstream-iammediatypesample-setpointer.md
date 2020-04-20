---
UID: NF:amstream.IAMMediaTypeSample.SetPointer
title: IAMMediaTypeSample::SetPointer (amstream.h)
description: Note  This interface is deprecated. New applications should not use it. The SetPointer method sets the pointer to the media sample's memory buffer.helpviewer_keywords: ["IAMMediaTypeSample interface [DirectShow]","SetPointer method","IAMMediaTypeSample.SetPointer","IAMMediaTypeSample::SetPointer","IAMMediaTypeSampleSetPointer","SetPointer","SetPointer method [DirectShow]","SetPointer method [DirectShow]","IAMMediaTypeSample interface","amstream/IAMMediaTypeSample::SetPointer","dshow.iammediatypesample_setpointer"]
old-location: dshow\iammediatypesample_setpointer.htm
tech.root: DirectShow
ms.assetid: fc7a04c5-3542-41e0-8abc-bb7b40bff2c9
ms.date: 12/05/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetPointer method, IAMMediaTypeSample.SetPointer, IAMMediaTypeSample::SetPointer, IAMMediaTypeSampleSetPointer, SetPointer, SetPointer method [DirectShow], SetPointer method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetPointer, dshow.iammediatypesample_setpointer
f1_keywords:
- amstream/IAMMediaTypeSample.SetPointer
dev_langs:
- c++
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
- IAMMediaTypeSample.SetPointer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaTypeSample::SetPointer


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetPointer</code> method sets the pointer to the media sample's memory buffer.




## -parameters




### -param pBuffer [in]

Pointer to a memory buffer allocated by the caller, or <b>NULL</b>.


### -param lSize [in]

Size of the buffer, in bytes.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>
 




## -remarks



If the value of the <i>pBuffer</i> parameter is <b>NULL</b>, the method allocates a memory block, with a size in bytes equal to the value of the <i>lSize</i> parameter. There is no guarantee that the memory has been initialized.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/amstream/nn-amstream-iammediatypesample">IAMMediaTypeSample Interface</a>
 

 

