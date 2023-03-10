---
UID: NF:tapi3if.IEnumCallHub.Reset
title: IEnumCallHub::Reset (tapi3if.h)
description: The Reset method resets to the beginning of the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumCallHub.Reset)
helpviewer_keywords: ["IEnumCallHub interface [TAPI 2.2]","Reset method","IEnumCallHub.Reset","IEnumCallHub::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumCallHub interface","_tapi3_ienumcallhub_reset","tapi3.ienumcallhub_reset","tapi3if/IEnumCallHub::Reset"]
old-location: tapi3\ienumcallhub_reset.htm
tech.root: tapi3
ms.assetid: 7e1c671b-ba2c-4ac2-ba3e-7a344d0834a4
ms.date: 12/05/2018
ms.keywords: IEnumCallHub interface [TAPI 2.2],Reset method, IEnumCallHub.Reset, IEnumCallHub::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumCallHub interface, _tapi3_ienumcallhub_reset, tapi3.ienumcallhub_reset, tapi3if/IEnumCallHub::Reset
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
 - IEnumCallHub::Reset
 - tapi3if/IEnumCallHub::Reset
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
 - IEnumCallHub.Reset
---

# IEnumCallHub::Reset


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

<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>
