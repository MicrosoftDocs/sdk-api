---
UID: NF:propidl.IEnumSTATPROPSETSTG.Clone
title: IEnumSTATPROPSETSTG::Clone (propidl.h)
description: The IEnumSTATPROPSETSTG::Clone method creates an enumerator that contains the same enumeration state as the current STATPROPSETSTG structure enumerator.
helpviewer_keywords: ["Clone","Clone method [Structured Storage]","Clone method [Structured Storage]","IEnumSTATPROPSETSTG interface","IEnumSTATPROPSETSTG interface [Structured Storage]","Clone method","IEnumSTATPROPSETSTG.Clone","IEnumSTATPROPSETSTG::Clone","propidlbase/IEnumSTATPROPSETSTG::Clone","stg.ienumstatpropsetstg_clone"]
old-location: stg\ienumstatpropsetstg_clone.htm
tech.root: Stg
ms.assetid: f875d5e9-fac0-4961-9570-342f55cf307e
ms.date: 08/02/2022
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATPROPSETSTG interface, IEnumSTATPROPSETSTG interface [Structured Storage],Clone method, IEnumSTATPROPSETSTG.Clone, IEnumSTATPROPSETSTG::Clone, propidlbase/IEnumSTATPROPSETSTG::Clone, stg.ienumstatpropsetstg_clone
req.header: propidl.h
req.include-header: Propidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
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
 - IEnumSTATPROPSETSTG::Clone
 - propidl/IEnumSTATPROPSETSTG::Clone
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
 - IEnumSTATPROPSETSTG.Clone
---

# IEnumSTATPROPSETSTG::Clone


## -description

The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the current <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point later. The new enumerator supports the same <a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> interface.

## -parameters

### -param ppenum [out]

    A pointer to the variable that receives the  <a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a> interface pointer. 

If the method does not succeed, the value of the <i>ppenum</i> parameter is undefined.

## -returns

This method supports return values listed in the following table.

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
