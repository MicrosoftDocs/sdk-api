---
UID: NF:objidl.IEnumSTATSTG.Reset
title: IEnumSTATSTG::Reset (objidl.h)
description: Resets the enumeration sequence to the beginning of the STATSTG structure array.
helpviewer_keywords: ["IEnumSTATSTG interface [Structured Storage]","Reset method","IEnumSTATSTG.Reset","IEnumSTATSTG::Reset","Reset","Reset method [Structured Storage]","Reset method [Structured Storage]","IEnumSTATSTG interface","objidl/IEnumSTATSTG::Reset","stg.ienumstatstg_reset"]
old-location: stg\ienumstatstg_reset.htm
tech.root: Stg
ms.assetid: 696aaa93-1b56-4baf-a6be-753c7d6f5456
ms.date: 12/05/2018
ms.keywords: IEnumSTATSTG interface [Structured Storage],Reset method, IEnumSTATSTG.Reset, IEnumSTATSTG::Reset, Reset, Reset method [Structured Storage], Reset method [Structured Storage],IEnumSTATSTG interface, objidl/IEnumSTATSTG::Reset, stg.ienumstatstg_reset
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumSTATSTG::Reset
 - objidl/IEnumSTATSTG::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG.Reset
---

# IEnumSTATSTG::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning of the <a href="/windows/desktop/api/objidl/ns-objidl-statstg">STATSTG</a> structure array.



## -returns

This method supports the S_OK return value.

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
The enumeration sequence was successfully reset to the beginning of the enumeration.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ienumstatstg">IEnumSTATSTG</a>
