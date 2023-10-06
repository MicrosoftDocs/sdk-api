---
UID: NF:dmusics.IDirectMusicSynth.GetFormat
title: IDirectMusicSynth::GetFormat (dmusics.h)
description: The GetFormat method retrieves information about the wave format.
helpviewer_keywords: ["GetFormat","GetFormat method [Audio Devices]","GetFormat method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","GetFormat method","IDirectMusicSynth.GetFormat","IDirectMusicSynth::GetFormat","audio.idirectmusicsynth_getformat","audmp-routines_4448775d-9737-4679-89ca-abfee56fa337.xml","dmusics/IDirectMusicSynth::GetFormat"]
old-location: audio\idirectmusicsynth_getformat.htm
tech.root: dshow
ms.assetid: 4fa55ff5-4f72-4f8b-bf11-64f07b054ff5
ms.date: 12/05/2018
ms.keywords: GetFormat, GetFormat method [Audio Devices], GetFormat method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],GetFormat method, IDirectMusicSynth.GetFormat, IDirectMusicSynth::GetFormat, audio.idirectmusicsynth_getformat, audmp-routines_4448775d-9737-4679-89ca-abfee56fa337.xml, dmusics/IDirectMusicSynth::GetFormat
req.header: dmusics.h
req.include-header: Dmusics.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectMusicSynth::GetFormat
 - dmusics/IDirectMusicSynth::GetFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dmusics.h
api_name:
 - IDirectMusicSynth.GetFormat
archived: true
---

# IDirectMusicSynth::GetFormat


## -description

The <code>GetFormat</code> method retrieves information about the wave format.

## -parameters

### -param pWaveFormatEx

Pointer to a caller-allocated <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure into which the method writes information about the format. This value can be <b>NULL</b>. For more information, see the following Remarks section.

### -param pdwWaveFormatExSize

Pointer to a caller-allocated DWORD variable specifying the size in bytes of the structure that <i>pWaveFormatEx</i> points to. For more information, see the following Remarks section.

## -returns

<code>GetFormat</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that one of the pointers is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or is not properly configured.

</td>
</tr>
</table>

## -remarks

The WAVEFORMATEX structure can have a variable length that depends on the details of the format. Therefore, before retrieving the format description, an application will first query the <b>IDirectMusicSynth</b> object for the size of the format by calling this method and specifying <b>NULL</b> for the <i>pWaveFormatEx</i> parameter. In this case, the synth should return the size of the structure in the <i>pdwWaveFormatExSize</i> parameter. The application can then allocate sufficient memory and call <code>IDirectMusicSynth::GetFormat</code> again to retrieve the format description.

If the <i>pWaveFormatEx</i> parameter is not <b>NULL</b>, DirectMusic writes, at most, <i>pdwWaveFormatExSize</i> bytes to <i>pWaveFormatEx</i>.

For more information, see the description of the <b>IDirectMusicPort</b> interface and <b>IDirectMusicPort::GetFormat</b> method in the Microsoft Windows SDK documentation.

## -see-also

<a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a>

