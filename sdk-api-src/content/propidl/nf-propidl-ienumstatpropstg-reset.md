---
UID: NF:propidl.IEnumSTATPROPSTG.Reset
title: IEnumSTATPROPSTG::Reset (propidl.h)
description: The IEnumSTATPROPSTG::Reset method resets the enumeration sequence to the beginning of the STATPROPSTG structure array. 
helpviewer_keywords: ["IEnumSTATPROPSTG interface [Structured Storage]","Reset method","IEnumSTATPROPSTG.Reset","IEnumSTATPROPSTG::Reset","Reset","Reset method [Structured Storage]","Reset method [Structured Storage]","IEnumSTATPROPSTG interface","propidlbase/IEnumSTATPROPSTG::Reset","stg.ienumstatpropstg_reset"]
old-location: stg\ienumstatpropstg_reset.htm
tech.root: Stg
ms.assetid: e742e3ee-6261-4d6d-85ca-8df770aa58ad
ms.date: 08/02/2022
ms.keywords: IEnumSTATPROPSTG interface [Structured Storage],Reset method, IEnumSTATPROPSTG.Reset, IEnumSTATPROPSTG::Reset, Reset, Reset method [Structured Storage], Reset method [Structured Storage],IEnumSTATPROPSTG interface, propidlbase/IEnumSTATPROPSTG::Reset, stg.ienumstatpropstg_reset
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
 - IEnumSTATPROPSTG::Reset
 - propidl/IEnumSTATPROPSTG::Reset
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
 - IEnumSTATPROPSTG.Reset
---

# IEnumSTATPROPSTG::Reset


## -description

The <b>Reset</b> method resets the enumeration sequence to the beginning of the <a href="/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a> structure array.



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
