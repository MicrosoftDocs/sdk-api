---
UID: NF:tapi3if.ITDetectTone.get_AppSpecific
title: ITDetectTone::get_AppSpecific (tapi3if.h)
description: The get_AppSpecific method retrieves the application-defined tag that identifies the tone to detect.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","get_AppSpecific method","ITDetectTone.get_AppSpecific","ITDetectTone::get_AppSpecific","_tapi3_itdetecttone_get_appspecific","get_AppSpecific","get_AppSpecific method [TAPI 2.2]","get_AppSpecific method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_get_appspecific","tapi3if/ITDetectTone::get_AppSpecific"]
old-location: tapi3\itdetecttone_get_appspecific.htm
tech.root: tapi3
ms.assetid: a3ffba50-664d-42d2-87b2-fe6943715e85
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],get_AppSpecific method, ITDetectTone.get_AppSpecific, ITDetectTone::get_AppSpecific, _tapi3_itdetecttone_get_appspecific, get_AppSpecific, get_AppSpecific method [TAPI 2.2], get_AppSpecific method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_get_appspecific, tapi3if/ITDetectTone::get_AppSpecific
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
 - ITDetectTone::get_AppSpecific
 - tapi3if/ITDetectTone::get_AppSpecific
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
 - ITDetectTone.get_AppSpecific
---

# ITDetectTone::get_AppSpecific


## -description

The 
<b>get_AppSpecific</b> method retrieves the application-defined tag that identifies the tone to detect.

## -parameters

### -param plAppSpecific [out]

Pointer to a value to receive the application-specific identifier for the tone. When the TAPI Server detects the tone, the value of this parameter is passed back to the application in the <b>TE_TONEEVENT</b> event.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_appspecific">put_AppSpecific</a>