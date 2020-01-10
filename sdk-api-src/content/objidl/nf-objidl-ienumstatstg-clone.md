---
UID: NF:objidl.IEnumSTATSTG.Clone
title: IEnumSTATSTG::Clone (objidl.h)
description: Creates a new enumerator that contains the same enumeration state as the current STATSTG structure enumerator.
old-location: stg\ienumstatstg_clone.htm
tech.root: Stg
ms.assetid: b6bc5dbd-7e09-4590-a7d4-d58fcd297f74
ms.date: 12/05/2018
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATSTG interface, IEnumSTATSTG interface [Structured Storage],Clone method, IEnumSTATSTG.Clone, IEnumSTATSTG::Clone, objidl/IEnumSTATSTG::Clone, stg.ienumstatstg_clone
f1_keywords:
- objidl/IEnumSTATSTG.Clone
dev_langs:
- c++
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IEnumSTATSTG.Clone
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATSTG::Clone


## -description


The <b>Clone</b> method creates a new enumerator that contains the same enumeration state as the current <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point at a later time. The new enumerator supports the same <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface.


## -parameters




### -param ppenum [out]

    A pointer to the variable that receives the  <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a> interface pointer. 

If the method is unsuccessful, the value of the <i>ppenum</i> parameter is undefined.


## -returns



This method supports the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppenum</i> parameter is <b>NULL</b>.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
An unexpected exception occurred.

</td>
</tr>
</table>
 



