---
UID: NF:tapi3if.ITCustomTone.get_Frequency
title: ITCustomTone::get_Frequency (tapi3if.h)
description: The get_Frequency method retrieves the frequency of the tone component to generate.
helpviewer_keywords: ["ITCustomTone interface [TAPI 2.2]","get_Frequency method","ITCustomTone.get_Frequency","ITCustomTone::get_Frequency","_tapi3_itcustomtone_get_frequency","get_Frequency","get_Frequency method [TAPI 2.2]","get_Frequency method [TAPI 2.2]","ITCustomTone interface","tapi3.itcustomtone_get_frequency","tapi3if/ITCustomTone::get_Frequency"]
old-location: tapi3\itcustomtone_get_frequency.htm
tech.root: tapi3
ms.assetid: 2521d754-234a-4ef0-a3b2-23cea999ad45
ms.date: 12/05/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],get_Frequency method, ITCustomTone.get_Frequency, ITCustomTone::get_Frequency, _tapi3_itcustomtone_get_frequency, get_Frequency, get_Frequency method [TAPI 2.2], get_Frequency method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_get_frequency, tapi3if/ITCustomTone::get_Frequency
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
 - ITCustomTone::get_Frequency
 - tapi3if/ITCustomTone::get_Frequency
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
 - ITCustomTone.get_Frequency
---

# ITCustomTone::get_Frequency


## -description

The 
<b>get_Frequency</b> method retrieves the frequency of the tone component to generate.

## -parameters

### -param plFrequency [out]

Pointer to a value to receive the frequency, in hertz, of the tone component.

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

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcustomtone">ITCustomTone</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-put_frequency">put_Frequency</a>