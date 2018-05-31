---
UID: NF:amstream.IAMMediaTypeSample.SetPointer
title: IAMMediaTypeSample::SetPointer
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetPointer method sets the pointer to the media sample's memory buffer.
old-location: dshow\iammediatypesample_setpointer.htm
old-project: DirectShow
ms.assetid: fc7a04c5-3542-41e0-8abc-bb7b40bff2c9
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetPointer method, IAMMediaTypeSample.SetPointer, IAMMediaTypeSample::SetPointer, IAMMediaTypeSampleSetPointer, SetPointer, SetPointer method [DirectShow], SetPointer method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetPointer, dshow.iammediatypesample_setpointer
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: AMSI_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IAMMediaTypeSample.SetPointer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

