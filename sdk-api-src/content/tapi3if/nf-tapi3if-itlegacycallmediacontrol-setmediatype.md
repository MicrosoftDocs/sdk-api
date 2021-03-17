---
UID: NF:tapi3if.ITLegacyCallMediaControl.SetMediaType
title: ITLegacyCallMediaControl::SetMediaType (tapi3if.h)
description: The SetMediaType method sets the media type(s) for the current call in its LINECALLINFO structure. For more information, see lineSetMediaMode.
helpviewer_keywords: ["ITLegacyCallMediaControl interface [TAPI 2.2]","SetMediaType method","ITLegacyCallMediaControl.SetMediaType","ITLegacyCallMediaControl::SetMediaType","SetMediaType","SetMediaType method [TAPI 2.2]","SetMediaType method [TAPI 2.2]","ITLegacyCallMediaControl interface","_tapi3_itlegacycallmediacontrol_setmediatype","tapi3.itlegacycallmediacontrol_setmediatype","tapi3if/ITLegacyCallMediaControl::SetMediaType"]
old-location: tapi3\itlegacycallmediacontrol_setmediatype.htm
tech.root: tapi3
ms.assetid: 627fe465-40f6-481e-9fd6-3fc3e2931e18
ms.date: 12/05/2018
ms.keywords: ITLegacyCallMediaControl interface [TAPI 2.2],SetMediaType method, ITLegacyCallMediaControl.SetMediaType, ITLegacyCallMediaControl::SetMediaType, SetMediaType, SetMediaType method [TAPI 2.2], SetMediaType method [TAPI 2.2],ITLegacyCallMediaControl interface, _tapi3_itlegacycallmediacontrol_setmediatype, tapi3.itlegacycallmediacontrol_setmediatype, tapi3if/ITLegacyCallMediaControl::SetMediaType
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
 - ITLegacyCallMediaControl::SetMediaType
 - tapi3if/ITLegacyCallMediaControl::SetMediaType
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
 - ITLegacyCallMediaControl.SetMediaType
---

# ITLegacyCallMediaControl::SetMediaType


## -description

The 
<b>SetMediaType</b> method sets the media type(s) for the current call in its 
<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a> structure. For more information, see 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetmediamode">lineSetMediaMode</a>.

## -parameters

### -param lMediaType [in]

Indicator of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

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
The associated call object is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lMediaType</i> parameter is not valid.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol">ITLegacyAddressMediaControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol">ITLegacyCallMediaControl</a>