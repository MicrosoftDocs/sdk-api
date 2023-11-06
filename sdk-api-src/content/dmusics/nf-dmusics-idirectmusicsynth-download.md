---
UID: NF:dmusics.IDirectMusicSynth.Download
title: IDirectMusicSynth::Download (dmusics.h)
description: The Download method downloads a wave or instrument definition to the synthesizer.
helpviewer_keywords: ["Download","Download method [Audio Devices]","Download method [Audio Devices]","IDirectMusicSynth interface","IDirectMusicSynth interface [Audio Devices]","Download method","IDirectMusicSynth.Download","IDirectMusicSynth::Download","audio.idirectmusicsynth_download","audmp-routines_5b59a66c-53b7-429c-81d1-8924f712b884.xml","dmusics/IDirectMusicSynth::Download"]
old-location: audio\idirectmusicsynth_download.htm
tech.root: dshow
ms.assetid: 2f36654c-25bf-47c3-a4d6-990d427bd1fc
ms.date: 12/05/2018
ms.keywords: Download, Download method [Audio Devices], Download method [Audio Devices],IDirectMusicSynth interface, IDirectMusicSynth interface [Audio Devices],Download method, IDirectMusicSynth.Download, IDirectMusicSynth::Download, audio.idirectmusicsynth_download, audmp-routines_5b59a66c-53b7-429c-81d1-8924f712b884.xml, dmusics/IDirectMusicSynth::Download
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
 - IDirectMusicSynth::Download
 - dmusics/IDirectMusicSynth::Download
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
 - IDirectMusicSynth.Download
archived: true
---

# IDirectMusicSynth::Download


## -description

The <code>Download</code> method downloads a wave or instrument definition to the synthesizer.

## -parameters

### -param phDownload

Output pointer for the download handle. This parameter points to a caller-allocated variable into which the method writes a handle identifying the download data. The caller uses this handle later to unload the data.

### -param pvData

Pointer to a continuous memory segment containing download data. For an overview of the data format, see the description of low-level DLS in the DirectMusic section of the Microsoft Windows SDK documentation.

### -param pbFree

Output pointer for a status value indicating whether the memory for the download data can be freed. This parameter points to a caller-allocated variable into which the method writes a Boolean value indicating whether the caller can free the storage pointed to by <i>pvData</i>. If <b>TRUE</b>, the application can safely free the memory after the return. If <b>FALSE</b>, the caller must keep the memory pointed to by <i>pvData</i> allocated until it is unloaded.

## -returns

<code>Download</code> returns S_OK if the call was successful. Otherwise, the method returns an appropriate error code. The following table shows some of the possible return status codes.

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
Indicates that one of the pointers is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the method is unable to download the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_SYNTHNOTCONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the synth is not open or not properly configured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOTMONO</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the wave chunk has more than one interleaved channel.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_BADARTICULATION</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad articulation chunk or link.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_BADINSTRUMENT</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad instrument chunk or link.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_BADWAVELINK</b></dt>
</dl>
</td>
<td width="60%">
Indicates a bad link to the wave download data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOARTICULATION</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the region in instrument has neither global nor local articulation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_NOTPCM</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the wave data is not PCM.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_BADWAVE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the wave header is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_BADOFFSETTABLE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the offset table contains errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DMUS_E_UNKNOWNDOWNLOAD</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the download data is neither instrument nor wave.

</td>
</tr>
</table>

## -remarks

The data is stored in a continuous chunk of memory, pointed to by <i>pvData</i>. However, at the head of the chunk are two data structures, which define the nature of the data to follow. These are the DMUS_DOWNLOADINFO and DMUS_OFFSETTABLE structures (described in Microsoft Windows SDK documentation). DMUS_DOWNLOADINFO is a header that describes how to parse the data, including its size and intention (wave or instrument.) DMUS_OFFSETTABLE provides a set of byte offsets into the data segment that follows. All parsing through the data is managed through this table. 

Whenever a structure in the data references another structure, it describes it by an index into the offset table. The offset table then converts it into a byte offset into the data. This allows the synthesizer to do bounds checking on all references, making the implementation more robust. In kernel-mode implementations, the driver can make its own private copy of the offset table, and so ensure that an application in user mode cannot alter its referencing and cause a crash.

The <b>dwDLType</b> member of DMUS_DOWNLOADINFO specifies the type of data being downloaded. It is set to DMUS_DOWNLOADINFO_INSTRUMENT for an instrument, DMUS_DOWNLOADINFO_WAVE for a wave. As new data types emerge, identifiers will be allocated for them. <b>dwDLId</b> holds a unique 32-bit identifier for the object. This identifier is used to connect objects together. In the case of level-1 DLS, the identifier is used to connect waves to instruments. The <b>dwNumOffsetTableEntries</b> member of DMUS_DOWNLOADINFO describes the number of entries in the DMUS_OFFSETTABLE structure, which follows. Finally, the <b>cbSize</b> member specifies the total size of the memory chunk that consists of DMUS_DOWNLOADINFO + DMUS_OFFSETTABLE + data chunk.

Note that the download memory is always padded with an extra 32 bytes. This allows synthesizer implementations that require additional padding at the end of loops for multipoint interpolation to fill the space after the end of a wave chunk with additional data, up to 32 bytes. This additional padding is reflected by <b>cbSize</b>.

Depending on the synthesizer implementation, the synthesizer might decide to use the memory in the download chunk. After all, if enough memory has been allocated to store a wave, that same memory can be used by the synthesizer to store it for playback. So the synthesizer has the option of retaining the memory, and it returns its decision in the <i>pbFree</i> parameter. If it does keep the memory, then the caller must not free it. Later, the <a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-unload">IDirectMusicSynth::Unload</a> method has a callback mechanism to handle asynchronous freeing of the memory once the unload request has been made.

## -see-also

<a href="/windows/desktop/api/dmusics/nn-dmusics-idirectmusicsynth">IDirectMusicSynth</a>



<a href="/windows/desktop/api/dmusics/nf-dmusics-idirectmusicsynth-unload">IDirectMusicSynth::Unload</a>