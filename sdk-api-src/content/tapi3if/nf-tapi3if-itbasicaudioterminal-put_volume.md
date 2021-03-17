---
UID: NF:tapi3if.ITBasicAudioTerminal.put_Volume
title: ITBasicAudioTerminal::put_Volume (tapi3if.h)
description: The put_Volume method sets the volume.
helpviewer_keywords: ["ITBasicAudioTerminal interface [TAPI 2.2]","put_Volume method","ITBasicAudioTerminal.put_Volume","ITBasicAudioTerminal::put_Volume","_tapi3_itbasicaudioterminal_put_volume","put_Volume","put_Volume method [TAPI 2.2]","put_Volume method [TAPI 2.2]","ITBasicAudioTerminal interface","tapi3.itbasicaudioterminal_put_volume","tapi3if/ITBasicAudioTerminal::put_Volume"]
old-location: tapi3\itbasicaudioterminal_put_volume.htm
tech.root: tapi3
ms.assetid: 6c611505-74b4-48fa-bb36-ec765cb24f96
ms.date: 12/05/2018
ms.keywords: ITBasicAudioTerminal interface [TAPI 2.2],put_Volume method, ITBasicAudioTerminal.put_Volume, ITBasicAudioTerminal::put_Volume, _tapi3_itbasicaudioterminal_put_volume, put_Volume, put_Volume method [TAPI 2.2], put_Volume method [TAPI 2.2],ITBasicAudioTerminal interface, tapi3.itbasicaudioterminal_put_volume, tapi3if/ITBasicAudioTerminal::put_Volume
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
 - ITBasicAudioTerminal::put_Volume
 - tapi3if/ITBasicAudioTerminal::put_Volume
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
 - ITBasicAudioTerminal.put_Volume
---

# ITBasicAudioTerminal::put_Volume


## -description

The 
<b>put_Volume</b> method sets the volume.

## -parameters

### -param lVolume [in]

The volume property is a value between 0 and FFFF, representing a set of logarithmic steps. Not all devices support as many distinguishable steps.

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
<dt><b>TAPI_E_NOTERMINALSELECTED</b></dt>
</dl>
</td>
<td width="60%">
A terminal must be selected before the volume can be adjusted.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal">ITBasicAudioTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasicaudioterminal-get_volume">get_Volume</a>