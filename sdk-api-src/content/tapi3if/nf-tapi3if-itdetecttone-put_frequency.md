---
UID: NF:tapi3if.ITDetectTone.put_Frequency
title: ITDetectTone::put_Frequency (tapi3if.h)
description: The put_Frequency method sets the frequency of the tone for which the TAPI Server should generate a tone event.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","put_Frequency method","ITDetectTone.put_Frequency","ITDetectTone::put_Frequency","_tapi3_itdetecttone_put_frequency","put_Frequency","put_Frequency method [TAPI 2.2]","put_Frequency method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_put_frequency","tapi3if/ITDetectTone::put_Frequency"]
old-location: tapi3\itdetecttone_put_frequency.htm
tech.root: tapi3
ms.assetid: 83895e55-61ab-464b-bb85-e81d15dd96e1
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],put_Frequency method, ITDetectTone.put_Frequency, ITDetectTone::put_Frequency, _tapi3_itdetecttone_put_frequency, put_Frequency, put_Frequency method [TAPI 2.2], put_Frequency method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_put_frequency, tapi3if/ITDetectTone::put_Frequency
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
 - ITDetectTone::put_Frequency
 - tapi3if/ITDetectTone::put_Frequency
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
 - ITDetectTone.put_Frequency
---

# ITDetectTone::put_Frequency


## -description

The 
<b>put_Frequency</b> method sets the frequency of the tone for which the TAPI Server should generate a tone event.

## -parameters

### -param Index [in]

Specifies the index of the tone to set.

### -param lFrequency [in]

Specifies the frequency, in hertz, of the tone. For more information, see the following Remarks section.

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

## -remarks

You can set up to three frequencies that make up the components of a tone. If fewer than three frequencies are required, specify a value of zero for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be used for silence detection.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-get_frequency">get_Frequency</a>