---
UID: NN:tapi3if.ITScriptableAudioFormat
title: ITScriptableAudioFormat
author: windows-sdk-content
description: The ITScriptableAudioFormat interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat.htm
tech.root: tapi
ms.assetid: 6b5d069a-044f-4bd4-b661-6100a2607107
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ITScriptableAudioFormat, ITScriptableAudioFormat interface [TAPI 2.2], ITScriptableAudioFormat interface [TAPI 2.2],described, _tapi3_itscriptableaudioformat, tapi3.itscriptableaudioformat, tapi3if/ITScriptableAudioFormat
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITScriptableAudioFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat interface


## -description


The 
<b>ITScriptableAudioFormat</b> interface is used by scriptable clients to get the audio format from, or set the audio format for, the track. The interface provides properties for each member from the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.

The 
<a href="https://msdn.microsoft.com/3677b85c-15a4-4960-88ad-18855349fedd">ITFileTrack::get_AudioFormatForScripting</a> and 
<a href="https://msdn.microsoft.com/80644b51-4b04-4299-a486-284e77583feb">ITFileTrack::get_EmptyAudioFormatForScripting</a> methods create the 
<b>ITScriptableAudioFormat</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITScriptableAudioFormat</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITScriptableAudioFormat</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITScriptableAudioFormat</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe54e1a5-ff8f-486d-90ba-3c7fc595ec1d">get_AvgBytesPerSec</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nAvgBytesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a98a3571-89bf-4625-b495-2d080c86c4b5">get_BitsPerSample</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>wBitsPerSample</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1f96d37e-af8b-4f0e-9bc0-467e3684fadb">get_BlockAlign</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nBlockAlign</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d92b08f-d108-4ea5-beac-cff2fad258cc">get_Channels</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nChannels</b> member in the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/073e4800-d84a-4f12-81ce-eba4a4e139fc">get_FormatTag</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>wFormatTag</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/614e0141-76dc-40ff-ad9b-a72b95e4a46d">get_SamplesPerSec</a>
</td>
<td align="left" width="63%">
Gets the value for the <b>nSamplesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca1b67b3-2dd0-47c1-9e91-ae94b6d78cc4">put_AvgBytesPerSec</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nAvgBytesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8e1038d6-122f-40c9-a6ab-57ae583ff9bc">put_BitsPerSample</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>wBitsPerSample</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc037229-4c5f-4778-af59-02e07d03a180">put_BlockAlign</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nBlockAlign</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/301fd17f-393b-46dd-9d76-1a1e34547629">put_Channels</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>nChannels</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a57eb237-189f-4c42-a1cd-9e70f53c3c4a">put_FormatTag</a>
</td>
<td align="left" width="63%">
Sets the value for the <b>wFormatTag</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9cf0d204-3623-4c93-9f75-39c39aa20f76">put_SamplesPerSec</a>
</td>
<td align="left" width="63%">
Sets the value of the <b>nSamplesPerSec</b> member in the <b>WAVEFORMATEX</b> structure.

</td>
</tr>
</table> 

