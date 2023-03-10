---
UID: NF:tapi3if.IEnumTerminalClass.Next
title: IEnumTerminalClass::Next (tapi3if.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumTerminalClass.Next)
helpviewer_keywords: ["IEnumTerminalClass interface [TAPI 2.2]","Next method","IEnumTerminalClass.Next","IEnumTerminalClass::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumTerminalClass interface","_tapi3_ienumterminalclass_next","tapi3.ienumterminalclass_next","tapi3if/IEnumTerminalClass::Next"]
old-location: tapi3\ienumterminalclass_next.htm
tech.root: tapi3
ms.assetid: 67ed4017-9cd2-4694-9853-c07bd4f81e0a
ms.date: 12/05/2018
ms.keywords: IEnumTerminalClass interface [TAPI 2.2],Next method, IEnumTerminalClass.Next, IEnumTerminalClass::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumTerminalClass interface, _tapi3_ienumterminalclass_next, tapi3.ienumterminalclass_next, tapi3if/IEnumTerminalClass::Next
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
 - IEnumTerminalClass::Next
 - tapi3if/IEnumTerminalClass::Next
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
 - IEnumTerminalClass.Next
---

# IEnumTerminalClass::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param celt [in]

Number of elements requested.

### -param pElements [out]

Pointer to list of elements returned.

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

## -see-also

<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
