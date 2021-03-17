---
UID: NF:tapi3if.ITCallHub.EnumerateCalls
title: ITCallHub::EnumerateCalls (tapi3if.h)
description: The EnumerateCalls method enumerates calls currently associated with the call hub. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Calls method.
helpviewer_keywords: ["EnumerateCalls","EnumerateCalls method [TAPI 2.2]","EnumerateCalls method [TAPI 2.2]","ITCallHub interface","ITCallHub interface [TAPI 2.2]","EnumerateCalls method","ITCallHub.EnumerateCalls","ITCallHub::EnumerateCalls","_tapi3_itcallhub_enumeratecalls","tapi3.itcallhub_enumeratecalls","tapi3if/ITCallHub::EnumerateCalls"]
old-location: tapi3\itcallhub_enumeratecalls.htm
tech.root: tapi3
ms.assetid: becacf70-0ae7-419c-a53f-c6172278d29f
ms.date: 12/05/2018
ms.keywords: EnumerateCalls, EnumerateCalls method [TAPI 2.2], EnumerateCalls method [TAPI 2.2],ITCallHub interface, ITCallHub interface [TAPI 2.2],EnumerateCalls method, ITCallHub.EnumerateCalls, ITCallHub::EnumerateCalls, _tapi3_itcallhub_enumeratecalls, tapi3.itcallhub_enumeratecalls, tapi3if/ITCallHub::EnumerateCalls
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
 - ITCallHub::EnumerateCalls
 - tapi3if/ITCallHub::EnumerateCalls
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
 - ITCallHub.EnumerateCalls
---

# ITCallHub::EnumerateCalls


## -description

The 
<b>EnumerateCalls</b> method enumerates calls currently associated with the call hub. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-get_calls">get_Calls</a> method.

## -parameters

### -param ppEnumCall [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
Insufficient memory exists to create the enumerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppEnumCall</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumcall">IEnumCall</a> interface returned by <b>ITCallHub::EnumerateCalls</b>. The application must call <b>Release</b> on the 
<b>IEnumCall</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>