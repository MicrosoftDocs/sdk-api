---
UID: NF:tapi3if.ITCustomTone.put_CadenceOff
title: ITCustomTone::put_CadenceOff (tapi3if.h)
description: The put_CadenceOff method sets the &quot;off&quot; duration of the cadence of the custom tone to generate.
helpviewer_keywords: ["ITCustomTone interface [TAPI 2.2]","put_CadenceOff method","ITCustomTone.put_CadenceOff","ITCustomTone::put_CadenceOff","_tapi3_itcustomtone_put_cadenceoff","put_CadenceOff","put_CadenceOff method [TAPI 2.2]","put_CadenceOff method [TAPI 2.2]","ITCustomTone interface","tapi3.itcustomtone_put_cadenceoff","tapi3if/ITCustomTone::put_CadenceOff"]
old-location: tapi3\itcustomtone_put_cadenceoff.htm
tech.root: tapi3
ms.assetid: 056e1ca5-2bce-4a69-9b30-2ac142bcb52b
ms.date: 12/05/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],put_CadenceOff method, ITCustomTone.put_CadenceOff, ITCustomTone::put_CadenceOff, _tapi3_itcustomtone_put_cadenceoff, put_CadenceOff, put_CadenceOff method [TAPI 2.2], put_CadenceOff method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_put_cadenceoff, tapi3if/ITCustomTone::put_CadenceOff
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
 - ITCustomTone::put_CadenceOff
 - tapi3if/ITCustomTone::put_CadenceOff
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
 - ITCustomTone.put_CadenceOff
---

# ITCustomTone::put_CadenceOff


## -description

The 
<b>put_CadenceOff</b> method sets the "off" duration of the cadence of the custom tone to generate.

## -parameters

### -param lCadenceOff [in]

Specifies the "off" duration, in milliseconds, of the cadence of the custom tone to generate. Zero means no off time, that is, a constant tone.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_cadenceoff">get_CadenceOff</a>