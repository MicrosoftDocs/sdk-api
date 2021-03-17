---
UID: NF:tapi3if.ITBasicAudioTerminal.get_Volume
title: ITBasicAudioTerminal::get_Volume (tapi3if.h)
description: The get_Volume method gets the volume.
helpviewer_keywords: ["ITBasicAudioTerminal interface [TAPI 2.2]","get_Volume method","ITBasicAudioTerminal.get_Volume","ITBasicAudioTerminal::get_Volume","_tapi3_itbasicaudioterminal_get_volume","get_Volume","get_Volume method [TAPI 2.2]","get_Volume method [TAPI 2.2]","ITBasicAudioTerminal interface","tapi3.itbasicaudioterminal_get_volume","tapi3if/ITBasicAudioTerminal::get_Volume"]
old-location: tapi3\itbasicaudioterminal_get_volume.htm
tech.root: tapi3
ms.assetid: 2d3a64fa-41b6-44c4-a67e-08113e771cc7
ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal interface [TAPI 2.2],get_Volume method, ITBasicAudioTerminal.get_Volume, ITBasicAudioTerminal::get_Volume, _tapi3_itbasicaudioterminal_get_volume, get_Volume, get_Volume method [TAPI 2.2], get_Volume method [TAPI 2.2],ITBasicAudioTerminal interface, tapi3.itbasicaudioterminal_get_volume, tapi3if/ITBasicAudioTerminal::get_Volume
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
 - ITBasicAudioTerminal::get_Volume
 - tapi3if/ITBasicAudioTerminal::get_Volume
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
 - ITBasicAudioTerminal.get_Volume
---

# ITBasicAudioTerminal::get_Volume


## -description

The 
<b>get_Volume</b> method gets the volume.

## -parameters

### -param plVolume [out]

Pointer to volume. The volume property is a value between 0 and FFFF, representing a set of logarithmic steps. Not all devices support as many distinguishable steps.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plVolume</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal">ITBasicAudioTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-put_volume">put_Volume</a>