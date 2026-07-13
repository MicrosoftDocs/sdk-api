---
UID: NF:tapi3if.IEnumCallHub.Next
title: IEnumCallHub::Next (tapi3if.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages. (IEnumCallHub.Next)
helpviewer_keywords: ["IEnumCallHub interface [TAPI 2.2]","Next method","IEnumCallHub.Next","IEnumCallHub::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumCallHub interface","_tapi3_ienumcallhub_next","tapi3.ienumcallhub_next","tapi3if/IEnumCallHub::Next"]
old-location: tapi3\ienumcallhub_next.htm
tech.root: tapi3
ms.assetid: 16469c1c-f12f-4941-9fd4-1413620c89bd
ms.date: 12/05/2018
ms.keywords: IEnumCallHub interface [TAPI 2.2],Next method, IEnumCallHub.Next, IEnumCallHub::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumCallHub interface, _tapi3_ienumcallhub_next, tapi3.ienumcallhub_next, tapi3if/IEnumCallHub::Next
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
 - IEnumCallHub::Next
 - tapi3if/IEnumCallHub::Next
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
 - IEnumCallHub.Next
---

# IEnumCallHub::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence. This method is hidden from Visual Basic and scripting languages.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> list of pointers returned.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a> interface returned by <b>IEnumCallHub::Next</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITCallHub</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>
