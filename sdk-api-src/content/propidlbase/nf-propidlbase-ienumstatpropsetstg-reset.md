---
UID: NF:propidlbase.IEnumSTATPROPSETSTG.Reset
title: IEnumSTATPROPSETSTG::Reset (propidlbase.h)
description: Resets the enumeration sequence to the beginning of the STATPROPSETSTG structure array.helpviewer_keywords: ["IEnumSTATPROPSETSTG interface [Structured Storage]","Reset method","IEnumSTATPROPSETSTG.Reset","IEnumSTATPROPSETSTG::Reset","Reset","Reset method [Structured Storage]","Reset method [Structured Storage]","IEnumSTATPROPSETSTG interface","propidlbase/IEnumSTATPROPSETSTG::Reset","stg.ienumstatpropsetstg_reset"]
old-location: stg\ienumstatpropsetstg_reset.htm
tech.root: Stg
ms.assetid: 41207be6-81ec-4dfc-a737-eb56792edb6d
ms.date: 12/05/2018
ms.keywords: IEnumSTATPROPSETSTG interface [Structured Storage],Reset method, IEnumSTATPROPSETSTG.Reset, IEnumSTATPROPSETSTG::Reset, Reset, Reset method [Structured Storage], Reset method [Structured Storage],IEnumSTATPROPSETSTG interface, propidlbase/IEnumSTATPROPSETSTG::Reset, stg.ienumstatpropsetstg_reset
f1_keywords:
- propidlbase/IEnumSTATPROPSETSTG.Reset
dev_langs:
- c++
req.header: propidlbase.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Ole32.dll
api_name:
- IEnumSTATPROPSETSTG.Reset
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumSTATPROPSETSTG::Reset


## -description


The <b>Reset</b> method resets the enumeration sequence to the beginning of the <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a> structure array.


## -parameters






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
 



