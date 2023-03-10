---
UID: NF:tapi3if.ITAddress.get_CurrentForwardInfo
title: ITAddress::get_CurrentForwardInfo (tapi3if.h)
description: The get_CurrentForwardInfo method gets a pointer to the current forwarding information object.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_CurrentForwardInfo method","ITAddress.get_CurrentForwardInfo","ITAddress::get_CurrentForwardInfo","_tapi3_itaddress_get_currentforwardinfo","get_CurrentForwardInfo","get_CurrentForwardInfo method [TAPI 2.2]","get_CurrentForwardInfo method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_currentforwardinfo","tapi3if/ITAddress::get_CurrentForwardInfo"]
old-location: tapi3\itaddress_get_currentforwardinfo.htm
tech.root: tapi3
ms.assetid: 7817ac03-d9fc-4042-ae7d-350ee6cbef53
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_CurrentForwardInfo method, ITAddress.get_CurrentForwardInfo, ITAddress::get_CurrentForwardInfo, _tapi3_itaddress_get_currentforwardinfo, get_CurrentForwardInfo, get_CurrentForwardInfo method [TAPI 2.2], get_CurrentForwardInfo method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_currentforwardinfo, tapi3if/ITAddress::get_CurrentForwardInfo
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
 - ITAddress::get_CurrentForwardInfo
 - tapi3if/ITAddress::get_CurrentForwardInfo
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
 - ITAddress.get_CurrentForwardInfo
---

# ITAddress::get_CurrentForwardInfo


## -description

The 
<b>get_CurrentForwardInfo</b> method gets a pointer to the current forwarding information object.

## -parameters

### -param ppForwardInfo [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

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
<dt><b>LINEERR_INVALPOINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppForwardInfo</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a> interface returned by <b>ITAddress::get_ForwardInfo</b>. The application must call <b>Release</b> on the 
<b>ITForwardInformation</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation">ITForwardInformation</a>