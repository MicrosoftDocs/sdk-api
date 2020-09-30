---
UID: NF:tapi3if.ITToneDetectionEvent.get_AppSpecific
title: ITToneDetectionEvent::get_AppSpecific (tapi3if.h)
description: The get_AppSpecific method gets the application-defined tag that identifies the tone associated with the tone detection event.
helpviewer_keywords: ["ITToneDetectionEvent interface [TAPI 2.2]","get_AppSpecific method","ITToneDetectionEvent.get_AppSpecific","ITToneDetectionEvent::get_AppSpecific","_tapi3_ittonedetectionevent_get_appspecific","get_AppSpecific","get_AppSpecific method [TAPI 2.2]","get_AppSpecific method [TAPI 2.2]","ITToneDetectionEvent interface","tapi3.ittonedetectionevent_get_appspecific","tapi3if/ITToneDetectionEvent::get_AppSpecific"]
old-location: tapi3\ittonedetectionevent_get_appspecific.htm
tech.root: tapi3
ms.assetid: 5c6c4890-7e65-4b4a-bc2f-ea3c11e5e85a
ms.date: 12/05/2018
ms.keywords: ITToneDetectionEvent interface [TAPI 2.2],get_AppSpecific method, ITToneDetectionEvent.get_AppSpecific, ITToneDetectionEvent::get_AppSpecific, _tapi3_ittonedetectionevent_get_appspecific, get_AppSpecific, get_AppSpecific method [TAPI 2.2], get_AppSpecific method [TAPI 2.2],ITToneDetectionEvent interface, tapi3.ittonedetectionevent_get_appspecific, tapi3if/ITToneDetectionEvent::get_AppSpecific
req.header: tapi3if.h
req.include-header: 
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
 - ITToneDetectionEvent::get_AppSpecific
 - tapi3if/ITToneDetectionEvent::get_AppSpecific
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
 - ITToneDetectionEvent.get_AppSpecific
---

# ITToneDetectionEvent::get_AppSpecific


## -description

The 
<b>get_AppSpecific</b> method gets the application-defined tag that identifies the tone associated with the tone detection event.

## -parameters

### -param plAppSpecific [out]

Pointer to a value to receive the application-specific identifier for the tone, as defined in the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a> object or in the 
<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a> structure.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plAppSpecific</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittonedetectionevent">ITToneDetectionEvent</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linemonitortone">LINEMONITORTONE</a>