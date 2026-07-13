---
UID: NF:propidl.IEnumSTATPROPSETSTG.Next
title: IEnumSTATPROPSETSTG::Next (propidl.h)
description: The IEnumSTATPROPSETSTG::Next method retrieves a specified number of STATPROPSETSTG structures that follow subsequently in the enumeration sequence.
helpviewer_keywords: ["IEnumSTATPROPSETSTG interface [Structured Storage]","Next method","IEnumSTATPROPSETSTG.Next","IEnumSTATPROPSETSTG::Next","Next","Next method [Structured Storage]","Next method [Structured Storage]","IEnumSTATPROPSETSTG interface","propidlbase/IEnumSTATPROPSETSTG::Next","stg.ienumstatpropsetstg_next"]
old-location: stg\ienumstatpropsetstg_next.htm
tech.root: Stg
ms.assetid: 3af3c518-3db4-4436-b1c1-86587ce8fbf3
ms.date: 08/02/2022
ms.keywords: IEnumSTATPROPSETSTG interface [Structured Storage],Next method, IEnumSTATPROPSETSTG.Next, IEnumSTATPROPSETSTG::Next, Next, Next method [Structured Storage], Next method [Structured Storage],IEnumSTATPROPSETSTG interface, propidlbase/IEnumSTATPROPSETSTG::Next, stg.ienumstatpropsetstg_next
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
 - IEnumSTATPROPSETSTG::Next
 - propidl/IEnumSTATPROPSETSTG::Next
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
 - IEnumSTATPROPSETSTG.Next
---

# IEnumSTATPROPSETSTG::Next


## -description

The <b>Next</b> method retrieves a specified number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures that follow subsequently in the enumeration sequence. If fewer than the requested number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures exist in the enumeration sequence, it retrieves the remaining <b>STATPROPSETSTG</b> structures.

## -parameters

### -param celt [in]

The number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures requested.

### -param rgelt [out]

An array of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures returned.

### -param pceltFetched [out]

The number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures  retrieved in the <i>rgelt</i> parameter.

## -returns

This method supports the following return values:

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
The number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures returned equals the number specified in the <i>celt</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of <a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structures returned is less than the number specified in the <i>celt</i> parameter.

</td>
</tr>
</table>
