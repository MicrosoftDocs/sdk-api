---
UID: NF:tapi3if.ITScriptableAudioFormat.get_Channels
title: ITScriptableAudioFormat::get_Channels (tapi3if.h)
description: The get_Channels method returns the value for the nChannels member in the WAVEFORMATEX structure.
helpviewer_keywords: ["ITScriptableAudioFormat interface [TAPI 2.2]","get_Channels method","ITScriptableAudioFormat.get_Channels","ITScriptableAudioFormat::get_Channels","_tapi3_itscriptableaudioformat_get_channels","get_Channels","get_Channels method [TAPI 2.2]","get_Channels method [TAPI 2.2]","ITScriptableAudioFormat interface","tapi3.itscriptableaudioformat_get_channels","tapi3if/ITScriptableAudioFormat::get_Channels"]
old-location: tapi3\itscriptableaudioformat_get_channels.htm
tech.root: tapi3
ms.assetid: 3d92b08f-d108-4ea5-beac-cff2fad258cc
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],get_Channels method, ITScriptableAudioFormat.get_Channels, ITScriptableAudioFormat::get_Channels, _tapi3_itscriptableaudioformat_get_channels, get_Channels, get_Channels method [TAPI 2.2], get_Channels method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_get_channels, tapi3if/ITScriptableAudioFormat::get_Channels
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
 - ITScriptableAudioFormat::get_Channels
 - tapi3if/ITScriptableAudioFormat::get_Channels
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
 - ITScriptableAudioFormat.get_Channels
---

# ITScriptableAudioFormat::get_Channels


## -description

The 
<b>get_Channels</b> method returns the value for the <b>nChannels</b> member in the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

## -parameters

### -param pVal [out]

Pointer to the value of the <b>nChannels</b> member in the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

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
The <i>pVal</i> argument is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-put_channels">put_Channels</a>