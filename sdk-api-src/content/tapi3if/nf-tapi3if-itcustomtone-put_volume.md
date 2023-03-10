---
UID: NF:tapi3if.ITCustomTone.put_Volume
title: ITCustomTone::put_Volume (tapi3if.h)
description: The put_Volume method sets the volume level at which to generate the tone.
helpviewer_keywords: ["ITCustomTone interface [TAPI 2.2]","put_Volume method","ITCustomTone.put_Volume","ITCustomTone::put_Volume","_tapi3_itcustomtone_put_volume","put_Volume","put_Volume method [TAPI 2.2]","put_Volume method [TAPI 2.2]","ITCustomTone interface","tapi3.itcustomtone_put_volume","tapi3if/ITCustomTone::put_Volume"]
old-location: tapi3\itcustomtone_put_volume.htm
tech.root: tapi3
ms.assetid: 2de6dbc3-9a3d-48e7-b9e1-56b3e25d1b60
ms.date: 12/05/2018
ms.keywords: ITCustomTone interface [TAPI 2.2],put_Volume method, ITCustomTone.put_Volume, ITCustomTone::put_Volume, _tapi3_itcustomtone_put_volume, put_Volume, put_Volume method [TAPI 2.2], put_Volume method [TAPI 2.2],ITCustomTone interface, tapi3.itcustomtone_put_volume, tapi3if/ITCustomTone::put_Volume
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
 - ITCustomTone::put_Volume
 - tapi3if/ITCustomTone::put_Volume
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
 - ITCustomTone.put_Volume
---

# ITCustomTone::put_Volume


## -description

The 
<b>put_Volume</b> method sets the volume level at which to generate the tone.

## -parameters

### -param lVolume [in]

Specifies the volume level for the tone. A value of 0x0000FFFF represents full volume; a value of 0x00000000 represents silence.

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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcustomtone-get_volume">get_Volume</a>