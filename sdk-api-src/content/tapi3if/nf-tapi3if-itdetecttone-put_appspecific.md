---
UID: NF:tapi3if.ITDetectTone.put_AppSpecific
title: ITDetectTone::put_AppSpecific (tapi3if.h)
description: The put_AppSpecific method sets the application-defined tag that identifies the tone to detect.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","put_AppSpecific method","ITDetectTone.put_AppSpecific","ITDetectTone::put_AppSpecific","_tapi3_itdetecttone_put_appspecific","put_AppSpecific","put_AppSpecific method [TAPI 2.2]","put_AppSpecific method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_put_appspecific","tapi3if/ITDetectTone::put_AppSpecific"]
old-location: tapi3\itdetecttone_put_appspecific.htm
tech.root: tapi3
ms.assetid: 0d008cda-bb01-4249-a0ca-a40d2daacbc4
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],put_AppSpecific method, ITDetectTone.put_AppSpecific, ITDetectTone::put_AppSpecific, _tapi3_itdetecttone_put_appspecific, put_AppSpecific, put_AppSpecific method [TAPI 2.2], put_AppSpecific method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_put_appspecific, tapi3if/ITDetectTone::put_AppSpecific
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
 - ITDetectTone::put_AppSpecific
 - tapi3if/ITDetectTone::put_AppSpecific
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
 - ITDetectTone.put_AppSpecific
---

# ITDetectTone::put_AppSpecific


## -description

The 
<b>put_AppSpecific</b> method sets the application-defined tag that identifies the tone to detect.

## -parameters

### -param lAppSpecific [in]

Specifies an application-specific tag that identifies the tone to detect. When the TAPI Server detects the tone, the value of this parameter is passed back to the application in the <b>TE_TONEEVENT</b> event.

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
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_appspecific">get_AppSpecific</a>