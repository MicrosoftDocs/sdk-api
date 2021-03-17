---
UID: NF:tapi3if.ITCustomTone.put_Frequency
title: ITCustomTone::put_Frequency (tapi3if.h)
description: The put_Frequency method sets the frequency of the tone component to generate.
helpviewer_keywords: ["ITCustomTone interface [TAPI 2.2]","put_Frequency method","ITCustomTone.put_Frequency","ITCustomTone::put_Frequency","_tapi3_itcustomtone_put_frequency","put_Frequency","put_Frequency method [TAPI 2.2]","put_Frequency method [TAPI 2.2]","ITCustomTone interface","tapi3.itcustomtone_put_frequency","tapi3if/ITCustomTone::put_Frequency"]
old-location: tapi3\itcustomtone_put_frequency.htm
tech.root: tapi3
ms.assetid: 1faae20a-40a7-48d7-9621-5f1761c28773
ms.date: 12/05/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],put_Frequency method, ITCustomTone.put_Frequency, ITCustomTone::put_Frequency, _tapi3_itcustomtone_put_frequency, put_Frequency, put_Frequency method [TAPI 2.2], put_Frequency method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_put_frequency, tapi3if/ITCustomTone::put_Frequency
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
 - ITCustomTone::put_Frequency
 - tapi3if/ITCustomTone::put_Frequency
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
 - ITCustomTone.put_Frequency
---

# ITCustomTone::put_Frequency


## -description

The 
<b>put_Frequency</b> method sets the frequency of the tone component to generate.

## -parameters

### -param lFrequency [in]

Specifies the frequency, in hertz, of the tone component.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_frequency">get_Frequency</a>