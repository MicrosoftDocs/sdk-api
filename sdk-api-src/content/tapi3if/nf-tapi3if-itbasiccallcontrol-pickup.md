---
UID: NF:tapi3if.ITBasicCallControl.Pickup
title: ITBasicCallControl::Pickup (tapi3if.h)
description: The Pickup method picks up a call alerting at the specified group identification.
helpviewer_keywords: ["ITBasicCallControl interface [TAPI 2.2]","Pickup method","ITBasicCallControl.Pickup","ITBasicCallControl::Pickup","Pickup","Pickup method [TAPI 2.2]","Pickup method [TAPI 2.2]","ITBasicCallControl interface","_tapi3_itbasiccallcontrol_pickup","tapi3.itbasiccallcontrol_pickup","tapi3if/ITBasicCallControl::Pickup"]
old-location: tapi3\itbasiccallcontrol_pickup.htm
tech.root: tapi3
ms.assetid: 25da3cf2-50f0-4f64-94ce-cf952e057376
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl interface [TAPI 2.2],Pickup method, ITBasicCallControl.Pickup, ITBasicCallControl::Pickup, Pickup, Pickup method [TAPI 2.2], Pickup method [TAPI 2.2],ITBasicCallControl interface, _tapi3_itbasiccallcontrol_pickup, tapi3.itbasiccallcontrol_pickup, tapi3if/ITBasicCallControl::Pickup
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
 - ITBasicCallControl::Pickup
 - tapi3if/ITBasicCallControl::Pickup
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
 - ITBasicCallControl.Pickup
---

# ITBasicCallControl::Pickup


## -description

The 
Pickup method picks up a call alerting at the specified group identification.

## -parameters

### -param pGroupID [in]

Pointer to a <b>BSTR</b> containing the group identifier to which the alerting station belongs.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Pickup did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pGroupID</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for the <i>pGroupID</i> parameter and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/Tapi/pickup-ovr">Pickup overview</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linepickup">linePickup</a>