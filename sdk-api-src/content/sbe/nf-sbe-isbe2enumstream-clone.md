---
UID: NF:sbe.ISBE2EnumStream.Clone
title: ISBE2EnumStream::Clone (sbe.h)
description: Creates a copy of the enumerator object. The copy starts with the same enumeration state as the original.helpviewer_keywords: ["Clone","Clone method [Microsoft TV Technologies]","Clone method [Microsoft TV Technologies]","ISBE2EnumStream interface","ISBE2EnumStream interface [Microsoft TV Technologies]","Clone method","ISBE2EnumStream.Clone","ISBE2EnumStream::Clone","mstv.isbe2enumstream_clone","sbe/ISBE2EnumStream::Clone"]
old-location: mstv\isbe2enumstream_clone.htm
tech.root: mstv
ms.assetid: d68daae6-2aef-4405-883b-a0e7ee6e5eb3
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Microsoft TV Technologies], Clone method [Microsoft TV Technologies],ISBE2EnumStream interface, ISBE2EnumStream interface [Microsoft TV Technologies],Clone method, ISBE2EnumStream.Clone, ISBE2EnumStream::Clone, mstv.isbe2enumstream_clone, sbe/ISBE2EnumStream::Clone
f1_keywords:
- sbe/ISBE2EnumStream.Clone
dev_langs:
- c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbe.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Sbe.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sbe.dll
api_name:
- ISBE2EnumStream.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISBE2EnumStream::Clone


## -description


Creates a copy of the enumerator object. The copy starts with the same enumeration state as the original.


## -parameters




### -param ppIEnumStream [out]

Receives a pointer to the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a> interface of the new enumerator object. This method allocates memory for the stream enumeration object. The caller is responsible for releasing the interface.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_POINTER</b></b></dt>
</dl>
</td>
<td width="60%">
Null pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_OUTOFMEMORY</b></b></dt>
</dl>
</td>
<td width="60%">
Out of memory for enumeration object.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-isbe2enumstream">ISBE2EnumStream</a>
 

 

