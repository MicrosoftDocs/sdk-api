---
UID: NF:tapi3if.ITForwardInformation.get_ForwardTypeDestination
title: ITForwardInformation::get_ForwardTypeDestination (tapi3if.h)
description: The get_ForwardTypeDestination method gets the destination for a forwarding mode.
helpviewer_keywords: ["ITForwardInformation interface [TAPI 2.2]","get_ForwardTypeDestination method","ITForwardInformation.get_ForwardTypeDestination","ITForwardInformation::get_ForwardTypeDestination","_tapi3_itforwardinformation_get_forwardtypedestination","get_ForwardTypeDestination","get_ForwardTypeDestination method [TAPI 2.2]","get_ForwardTypeDestination method [TAPI 2.2]","ITForwardInformation interface","tapi3.itforwardinformation_get_forwardtypedestination","tapi3if/ITForwardInformation::get_ForwardTypeDestination"]
old-location: tapi3\itforwardinformation_get_forwardtypedestination.htm
tech.root: tapi3
ms.assetid: 84a5737c-3bcd-4fdf-9a51-ef726fe71682
ms.date: 12/05/2018
ms.keywords: ITForwardInformation interface [TAPI 2.2],get_ForwardTypeDestination method, ITForwardInformation.get_ForwardTypeDestination, ITForwardInformation::get_ForwardTypeDestination, _tapi3_itforwardinformation_get_forwardtypedestination, get_ForwardTypeDestination, get_ForwardTypeDestination method [TAPI 2.2], get_ForwardTypeDestination method [TAPI 2.2],ITForwardInformation interface, tapi3.itforwardinformation_get_forwardtypedestination, tapi3if/ITForwardInformation::get_ForwardTypeDestination
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
 - ITForwardInformation::get_ForwardTypeDestination
 - tapi3if/ITForwardInformation::get_ForwardTypeDestination
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
 - ITForwardInformation.get_ForwardTypeDestination
---

# ITForwardInformation::get_ForwardTypeDestination


## -description

The 
<b>get_ForwardTypeDestination</b> method gets the destination for a forwarding mode.

## -parameters

### -param ForwardType [in]

<a href="/windows/desktop/Tapi/lineforwardmode--constants">Line forward mode</a>.

### -param ppDestAddress [out]

Pointer to <b>BSTR</b> representation of destination address.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDestAddress</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDestAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDestAddress</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>