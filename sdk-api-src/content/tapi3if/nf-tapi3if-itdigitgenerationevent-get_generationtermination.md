---
UID: NF:tapi3if.ITDigitGenerationEvent.get_GenerationTermination
title: ITDigitGenerationEvent::get_GenerationTermination (tapi3if.h)
description: The get_GenerationTermination method gets the digit or digits that indicate the end of the generated digit series.
helpviewer_keywords: ["ITDigitGenerationEvent interface [TAPI 2.2]","get_GenerationTermination method","ITDigitGenerationEvent.get_GenerationTermination","ITDigitGenerationEvent::get_GenerationTermination","_tapi3_itdigitgenerationevent_get_generationtermination","get_GenerationTermination","get_GenerationTermination method [TAPI 2.2]","get_GenerationTermination method [TAPI 2.2]","ITDigitGenerationEvent interface","tapi3.itdigitgenerationevent_get_generationtermination","tapi3if/ITDigitGenerationEvent::get_GenerationTermination"]
old-location: tapi3\itdigitgenerationevent_get_generationtermination.htm
tech.root: tapi3
ms.assetid: 70e8c932-a157-455e-b340-d7e4eb19823c
ms.date: 12/05/2018
ms.keywords: ITDigitGenerationEvent interface [TAPI 2.2],get_GenerationTermination method, ITDigitGenerationEvent.get_GenerationTermination, ITDigitGenerationEvent::get_GenerationTermination, _tapi3_itdigitgenerationevent_get_generationtermination, get_GenerationTermination, get_GenerationTermination method [TAPI 2.2], get_GenerationTermination method [TAPI 2.2],ITDigitGenerationEvent interface, tapi3.itdigitgenerationevent_get_generationtermination, tapi3if/ITDigitGenerationEvent::get_GenerationTermination
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
 - ITDigitGenerationEvent::get_GenerationTermination
 - tapi3if/ITDigitGenerationEvent::get_GenerationTermination
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
 - ITDigitGenerationEvent.get_GenerationTermination
---

# ITDigitGenerationEvent::get_GenerationTermination


## -description

The 
<b>get_GenerationTermination</b> method gets the digit or digits that indicate the end of the generated digit series.

## -parameters

### -param plGenerationTermination [out]

Pointer to digit or digits that indicate the end of the generated digit series.

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
The <i>plGenerationTermination</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitgenerationevent">ITDigitGenerationEvent</a>