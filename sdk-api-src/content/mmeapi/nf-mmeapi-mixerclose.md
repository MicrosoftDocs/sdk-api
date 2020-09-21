---
UID: NF:mmeapi.mixerClose
title: mixerClose function (mmeapi.h)
description: The mixerClose function closes the specified mixer device.
helpviewer_keywords: ["_win32_mixerClose","mixerClose","mixerClose function [Windows Multimedia]","mmeapi/mixerClose","multimedia.mixerclose"]
old-location: multimedia\mixerclose.htm
tech.root: Multimedia
ms.assetid: d92a9bb0-9761-471b-85d2-af0bcdbbda34
ms.date: 12/05/2018
ms.keywords: _win32_mixerClose, mixerClose, mixerClose function [Windows Multimedia], mmeapi/mixerClose, multimedia.mixerclose
req.header: mmeapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mixerClose
 - mmeapi/mixerClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - mixerClose
---

# mixerClose function


## -description

The <b>mixerClose</b> function closes the specified mixer device.

## -parameters

### -param hmx

Handle to the mixer device. This handle must have been returned successfully by the <a href="/previous-versions/dd757308(v=vs.85)">mixerOpen</a> function. If <b>mixerClose</b> is successful, <i>hmx</i> is no longer valid.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
Specified device handle is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/audio-mixer-functions">Audio Mixer Functions</a>



<a href="/windows/desktop/Multimedia/audio-mixers">Audio Mixers</a>