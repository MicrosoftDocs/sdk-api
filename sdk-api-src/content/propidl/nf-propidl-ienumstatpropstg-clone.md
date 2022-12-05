---
UID: NF:propidl.IEnumSTATPROPSTG.Clone
title: IEnumSTATPROPSTG::Clone (propidl.h)
description: The IEnumSTATPROPSTG::Clone method creates an enumerator that contains the same enumeration state as the current STATPROPSTG structure enumerator.
helpviewer_keywords: ["Clone","Clone method [Structured Storage]","Clone method [Structured Storage]","IEnumSTATPROPSTG interface","IEnumSTATPROPSTG interface [Structured Storage]","Clone method","IEnumSTATPROPSTG.Clone","IEnumSTATPROPSTG::Clone","propidlbase/IEnumSTATPROPSTG::Clone","stg.ienumstatpropstg_clone"]
old-location: stg\ienumstatpropstg_clone.htm
tech.root: Stg
ms.assetid: e06e109a-3f9d-4b08-bde9-888cb795287c
ms.date: 08/02/2022
ms.keywords: Clone, Clone method [Structured Storage], Clone method [Structured Storage],IEnumSTATPROPSTG interface, IEnumSTATPROPSTG interface [Structured Storage],Clone method, IEnumSTATPROPSTG.Clone, IEnumSTATPROPSTG::Clone, propidlbase/IEnumSTATPROPSTG::Clone, stg.ienumstatpropstg_clone
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
 - IEnumSTATPROPSTG::Clone
 - propidl/IEnumSTATPROPSTG::Clone
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
 - IEnumSTATPROPSTG.Clone
---

# IEnumSTATPROPSTG::Clone


## -description

The <b>Clone</b> method creates an enumerator that contains the same enumeration state as the current <a href="/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structure enumerator. Using this method, a client can record a particular point in the enumeration sequence and then return to that point later. The new enumerator supports the same <a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> interface.

## -parameters

### -param ppenum [out]

    A pointer to the variable that receives the  <a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a> interface pointer. 

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
