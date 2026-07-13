---
UID: NF:tapi3if.IEnumCall.Reset
title: IEnumCall::Reset (tapi3if.h)
description: The Reset method resets to the beginning of the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumCall.Reset)
helpviewer_keywords: ["IEnumCall interface [TAPI 2.2]","Reset method","IEnumCall.Reset","IEnumCall::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumCall interface","_tapi3_ienumcall_reset","tapi3.ienumcall_reset","tapi3if/IEnumCall::Reset"]
old-location: tapi3\ienumcall_reset.htm
tech.root: tapi3
ms.assetid: 9aa41bab-c575-440b-b1ff-bdbdde68da36
ms.date: 12/05/2018
ms.keywords: IEnumCall interface [TAPI 2.2],Reset method, IEnumCall.Reset, IEnumCall::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumCall interface, _tapi3_ienumcall_reset, tapi3.ienumcall_reset, tapi3if/IEnumCall::Reset
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumCall::Reset
 - tapi3if/IEnumCall::Reset
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - IEnumCall.Reset
---

# IEnumCall::Reset


## -description

The 
<b>Reset</b> method resets to the beginning of the enumeration sequence. This method is hidden from Visual Basic and scripting languages.



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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>
