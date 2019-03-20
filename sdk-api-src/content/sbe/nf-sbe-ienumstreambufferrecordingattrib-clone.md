---
UID: NF:sbe.IEnumStreamBufferRecordingAttrib.Clone
title: IEnumStreamBufferRecordingAttrib::Clone (sbe.h)
author: windows-sdk-content
description: The Clone method makes a copy of the enumerator object. The returned object starts with the same enumeration state as the original.
old-location: mstv\ienumstreambufferrecordingattrib_clone.htm
tech.root: mstv
ms.assetid: 542a8b5d-641a-4ffb-9c8b-7232b1723a07
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],IEnumStreamBufferRecordingAttrib interface, IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],Clone method, IEnumStreamBufferRecordingAttrib.Clone, IEnumStreamBufferRecordingAttrib::Clone, IEnumStreamBufferRecordingAttribClone, mstv.ienumstreambufferrecordingattrib_clone, sbe/IEnumStreamBufferRecordingAttrib::Clone
ms.topic: method
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
 - Sbe.h
api_name:
 - IEnumStreamBufferRecordingAttrib.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumStreamBufferRecordingAttrib::Clone


## -description


The <b>Clone</b> method makes a copy of the enumerator object. The returned object starts with the same enumeration state as the original.


## -parameters




### -param ppIEnumStreamBufferAttrib [out]

Address of a variable that receives a pointer to the <b>IEnumStreamBufferRecordingAttrib</b> interface of the new enumerator.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/668d2e04-74fa-41d7-b238-ec737a4441ca">IEnumStreamBufferRecordingAttrib Interface</a>
 

 

