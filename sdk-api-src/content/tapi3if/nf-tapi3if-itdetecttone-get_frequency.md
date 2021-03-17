---
UID: NF:tapi3if.ITDetectTone.get_Frequency
title: ITDetectTone::get_Frequency (tapi3if.h)
description: The get_Frequency method retrieves the frequency of the tone for which the TAPI Server generates a tone event.
helpviewer_keywords: ["ITDetectTone interface [TAPI 2.2]","get_Frequency method","ITDetectTone.get_Frequency","ITDetectTone::get_Frequency","_tapi3_itdetecttone_get_frequency","get_Frequency","get_Frequency method [TAPI 2.2]","get_Frequency method [TAPI 2.2]","ITDetectTone interface","tapi3.itdetecttone_get_frequency","tapi3if/ITDetectTone::get_Frequency"]
old-location: tapi3\itdetecttone_get_frequency.htm
tech.root: tapi3
ms.assetid: a7137eba-c863-4125-9602-14bfba814b2a
ms.date: 12/05/2018
ms.keywords: ITDetectTone interface [TAPI 2.2],get_Frequency method, ITDetectTone.get_Frequency, ITDetectTone::get_Frequency, _tapi3_itdetecttone_get_frequency, get_Frequency, get_Frequency method [TAPI 2.2], get_Frequency method [TAPI 2.2],ITDetectTone interface, tapi3.itdetecttone_get_frequency, tapi3if/ITDetectTone::get_Frequency
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
 - ITDetectTone::get_Frequency
 - tapi3if/ITDetectTone::get_Frequency
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
 - ITDetectTone.get_Frequency
---

# ITDetectTone::get_Frequency


## -description

The 
<b>get_Frequency</b> method retrieves the frequency of the tone for which the TAPI Server generates a tone event.

## -parameters

### -param Index [in]

Specifies the index of the tone.

### -param plFrequency [out]

Pointer to a value to receive the frequency, in hertz, of the tone. For more information, see the following Remarks section.

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
The <i>plFrequency</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

You can set up to three frequencies that make up the components of a tone. If fewer than three frequencies are required, specify a value of zero for the unused frequencies. A tone with all three frequencies set to zero is interpreted as silence and can be used for silence detection.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdetecttone">ITDetectTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itdetecttone-put_frequency">put_Frequency</a>