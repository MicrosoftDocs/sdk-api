---
UID: NE:strmif.tagTVAudioMode
title: TVAudioMode (strmif.h)
description: Specifies the mode of a TV audio control.
helpviewer_keywords: ["AMTVAUDIO_MODE_LANG_A","AMTVAUDIO_MODE_LANG_B","AMTVAUDIO_MODE_LANG_C","AMTVAUDIO_MODE_MONO","AMTVAUDIO_MODE_STEREO","AMTVAUDIO_PRESET_LANG_A","AMTVAUDIO_PRESET_LANG_B","AMTVAUDIO_PRESET_LANG_C","AMTVAUDIO_PRESET_STEREO","TVAudioMode","TVAudioMode enumeration [DirectShow]","TVAudioModeEnumeration","dshow.tvaudiomode","strmif/AMTVAUDIO_MODE_LANG_A","strmif/AMTVAUDIO_MODE_LANG_B","strmif/AMTVAUDIO_MODE_LANG_C","strmif/AMTVAUDIO_MODE_MONO","strmif/AMTVAUDIO_MODE_STEREO","strmif/AMTVAUDIO_PRESET_LANG_A","strmif/AMTVAUDIO_PRESET_LANG_B","strmif/AMTVAUDIO_PRESET_LANG_C","strmif/AMTVAUDIO_PRESET_STEREO","strmif/TVAudioMode"]
old-location: dshow\tvaudiomode.htm
tech.root: dshow
ms.assetid: 70e26550-0a8f-484e-b919-cfefdcf95f6b
ms.date: 12/05/2018
ms.keywords: AMTVAUDIO_MODE_LANG_A, AMTVAUDIO_MODE_LANG_B, AMTVAUDIO_MODE_LANG_C, AMTVAUDIO_MODE_MONO, AMTVAUDIO_MODE_STEREO, AMTVAUDIO_PRESET_LANG_A, AMTVAUDIO_PRESET_LANG_B, AMTVAUDIO_PRESET_LANG_C, AMTVAUDIO_PRESET_STEREO, TVAudioMode, TVAudioMode enumeration [DirectShow], TVAudioModeEnumeration, dshow.tvaudiomode, strmif/AMTVAUDIO_MODE_LANG_A, strmif/AMTVAUDIO_MODE_LANG_B, strmif/AMTVAUDIO_MODE_LANG_C, strmif/AMTVAUDIO_MODE_MONO, strmif/AMTVAUDIO_MODE_STEREO, strmif/AMTVAUDIO_PRESET_LANG_A, strmif/AMTVAUDIO_PRESET_LANG_B, strmif/AMTVAUDIO_PRESET_LANG_C, strmif/AMTVAUDIO_PRESET_STEREO, strmif/TVAudioMode
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TVAudioMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagTVAudioMode
 - strmif/tagTVAudioMode
 - TVAudioMode
 - strmif/TVAudioMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Strmif.h
api_name:
 - TVAudioMode
---

# TVAudioMode enumeration


## -description

Specifies the mode of a TV audio control.

## -enum-fields

### -field AMTVAUDIO_MODE_MONO:0x1

Mono.

### -field AMTVAUDIO_MODE_STEREO:0x2

Stereo.

### -field AMTVAUDIO_MODE_LANG_A:0x10

Language A: Main audio channel.

### -field AMTVAUDIO_MODE_LANG_B:0x20

Languag B: Secondary audio program (SAP).

### -field AMTVAUDIO_MODE_LANG_C:0x40

Language C: Either a third language, or the main audio program plus the SAP (for example, English from one speaker and Japanese from the other speaker).

### -field AMTVAUDIO_PRESET_STEREO:0x200

Stereo preset.

### -field AMTVAUDIO_PRESET_LANG_A:0x1000

Languag A preset.

### -field AMTVAUDIO_PRESET_LANG_B:0x2000

Language B preset.

### -field AMTVAUDIO_PRESET_LANG_C:0x4000

Language C preset.

## -remarks

The <b>TVAudioMode</b> flags fall into two groups.

<ul>
<li>Bits 0 - 7: Mode flags. These flags include mono/stereo and language (A, B, or C).</li>
<li>Bits 8 and higher: Preset flags. </li>
</ul>
<div class="alert"><b>Note</b>  The preset flags require Windows Vista or later.</div>
<div> </div>
The mode flags represent the tuner's current audio mode. The preset flags represent settings that can take effect in the future, if the audio signal changes. Often, the secondary audio program is not available, or is available only in mono. An application can use the preset flags to store the user's preferred language while providing a reasonable experience when that language is not available.

The following remarks describe how the <a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio</a> methods interpret these flags.


<a href="/windows/desktop/api/strmif/nf-strmif-iamtvaudio-put_tvaudiomode">IAMTVAudio::put_TVAudioMode</a>:
        

<ul>
<li>If you set a mode flag, the tuner switches to that mode immediately. If the mode is not immediately available, the method fails.</li>
<li>If you set a preset flag, the driver switches to that mode immediately if possible; otherwise, the driver stores the request. If the requested mode becomes available later, the driver switches to that mode. The driver maintains the preset flags across program changes or channel changes. A preset mode fails only if the tuner cannot support that mode. It never fails due to the contents of the audio signal.</li>
</ul>
You may combine one language mode flag (<b>AMTVAUDIO_MODE_LANG_A</b>, <b>AMTVAUDIO_MODE_LANG_B</b>, or <b>AMTVAUDIO_MODE_LANG_C</b>) with one stereo/mono flag (<b>AMTVAUDIO_MODE_MONO</b> or <b>AMTVAUDIO_MODE_STEREO</b>). Other combinations of mode flags are not valid. For example, <b>AMTVAUDIO_MODE_LANG_A</b> | <b>AMTVAUDIO_MODE_LANG_B</b> is not valid.

You may combine more than one preset flag. The driver attempts them in the following order:

<ol>
<li>Language C</li>
<li>Language B</li>
<li>Language A</li>
<li>Stereo</li>
</ol>
You may combine mode flags and preset flags, but you cannot combine a mode flag and a preset flag for the same language. For example, <b>AMTVAUDIO_MODE_LANG_A</b> | <b>AMTVAUDIO_PRESET_LANG_A</b> is not valid. Mode flags have priority over preset flags.

If the method fails for any reason, the state of the tuner — that is, the current mode plus the stored presets — does not change.

Except for language C, the tuner always streams the same language over both audio channels.

Example: The caller sets <b>AMTVAUDIO_PRESET_STEREO</b> | <b>AMTVAUDIO_PRESET_LANG_B</b>. Suppose the current program is available in language A with stereo or language B with mono. The driver selects language B (mono), because that flag takes precedence. Later, the program switches to a commercial that is only available in language A. The driver switches to language A, because language B is not available. When the program resumes, the driver switches back to language B.


<a href="/windows/desktop/api/strmif/nf-strmif-iamtvaudio-getavailabletvaudiomodes">IAMTVAudio::GetAvailableTVAudioModes</a>: This method returns the modes that are currently available in the signal. This method never returns preset flags.


<a href="/windows/desktop/api/strmif/nf-strmif-iamtvaudio-gethardwaresupportedtvaudiomodes">IAMTVAudio::GetHardwareSupportedTVAudioModes</a>: This method returns all of the modes supported by the hardware, including preset modes.


<a href="/windows/desktop/api/strmif/nf-strmif-iamtvaudio-get_tvaudiomode">IAMTVAudio::get_TVAudioMode</a>: This method returns the current mode. This method never returns preset flags.

<h3><a id="Mask_Constants"></a><a id="mask_constants"></a><a id="MASK_CONSTANTS"></a>Mask Constants</h3>
The following constants are defined in Strmif.h:
          


``` syntax
#define TVAUDIO_MODE_MASK 0x000000ff
#define TVAUDIO_PRESET_MASK 0x0000ff00
```

You can use <b>TVAUDIO_MODE_MASK</b> to select mode flags and <b>TVAUDIO_PRESET_MASK</b> to select preset flags:
          

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD ModeFlags(DWORD AudioMode)
{
    return AudioMode &amp; TVAUDIO_MODE_MASK;
}   

DWORD PresetFlags(DWORD AudioMode)
{
    return AudioMode &amp; TVAUDIO_PRESET_MASK;
}</pre>
</td>
</tr>
</table></span></div>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>
