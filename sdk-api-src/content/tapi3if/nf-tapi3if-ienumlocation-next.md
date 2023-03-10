---
UID: NF:tapi3if.IEnumLocation.Next
title: IEnumLocation::Next (tapi3if.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumLocation.Next)
helpviewer_keywords: ["IEnumLocation interface [TAPI 2.2]","Next method","IEnumLocation.Next","IEnumLocation::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumLocation interface","_tapi3_ienumlocation_next","tapi3.ienumlocation_next","tapi3if/IEnumLocation::Next"]
old-location: tapi3\ienumlocation_next.htm
tech.root: tapi3
ms.assetid: e9fe8747-5c65-47fd-9e1a-2387971bdf15
ms.date: 12/05/2018
ms.keywords: IEnumLocation interface [TAPI 2.2],Next method, IEnumLocation.Next, IEnumLocation::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumLocation interface, _tapi3_ienumlocation_next, tapi3.ienumlocation_next, tapi3if/IEnumLocation::Next
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
 - IEnumLocation::Next
 - tapi3if/IEnumLocation::Next
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
 - IEnumLocation.Next
---

# IEnumLocation::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a> pointer.

### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

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

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a> interface returned by <b>IEnumLocation::Next</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITLocationInfo</b> interface to free resources associated with it.
