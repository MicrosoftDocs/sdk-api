---
UID: NS:xapo.XAPO_REGISTRATION_PROPERTIES
title: XAPO_REGISTRATION_PROPERTIES (xapo.h)
description: Describes general characteristics of an XAPO. Used with IXAPO::GetRegistrationProperties, CXAPOParametersBase::CXAPOParametersBase, and CXAPOBase::CXAPOBase.
helpviewer_keywords: ["XAPO_REGISTRATION_PROPERTIES","XAPO_REGISTRATION_PROPERTIES structure [XAudio2 Audio Mixing APIs]","xapo/XAPO_REGISTRATION_PROPERTIES","xaudio2.xapo_registration_properties"]
old-location: xaudio2\xapo_registration_properties.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xapo.XAPO_REGISTRATION_PROPERTIES
ms.date: 12/05/2018
ms.keywords: XAPO_REGISTRATION_PROPERTIES, XAPO_REGISTRATION_PROPERTIES structure [XAudio2 Audio Mixing APIs], xapo/XAPO_REGISTRATION_PROPERTIES, xaudio2.xapo_registration_properties
req.header: xapo.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: XAPO_REGISTRATION_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XAPO_REGISTRATION_PROPERTIES
 - xapo/XAPO_REGISTRATION_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xapo.h
api_name:
 - XAPO_REGISTRATION_PROPERTIES
---

# XAPO_REGISTRATION_PROPERTIES structure


## -description

Describes general characteristics of an XAPO. Used with 
	 <a href="/windows/desktop/api/xapo/nf-xapo-ixapo-getregistrationproperties">IXAPO::GetRegistrationProperties</a>, <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapoparametersbase-cxapoparametersbase">CXAPOParametersBase::CXAPOParametersBase</a>, and 
	 <a href="/windows/desktop/api/xapobase/nf-xapobase-cxapobase-cxapobase">CXAPOBase::CXAPOBase</a>.

## -struct-fields

### -field clsid

COM class ID for use with the CoCreateInstance function.

### -field FriendlyName

Friendly name, a unicode string.

### -field CopyrightInfo

Copyright information, a unicode string.

### -field MajorVersion

Major version number.

### -field MinorVersion

Minor version number.

### -field Flags

XAPO property flags that describe the general characteristics of process behavior. These flags are described in the following table. 
	 

<table>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
<tr>
<td>XAPO_FLAG_INPLACE_SUPPORTED</td>
<td>
XAPO supports in-place processing: the input stream buffer and output stream buffer 
            can be the same buffer depending on the input.

For example, consider an effect which may be ran in stereo to 5.1 mode or
            mono to mono mode.  When set to stereo to 5.1, it will be run with separate
            input and output buffers as format conversion is not permitted in-place.
            However, if configured to run mono to mono, the same XAPO can be run
            in-place.  Thus the same implementation may be conveniently reused
            for various input/output configurations, while taking advantage of
            in-place processing when possible.

</td>
</tr>
<tr>
<td>XAPO_FLAG_INPLACE_REQUIRED</td>
<td>XAPO requires in-place processing: the input stream buffer and output stream buffer must 
            be the same buffer.  When the XAPO_FLAG_INPLACE_REQUIRED is used the XAPO cannot perform 
            format conversions.</td>
</tr>
<tr>
<td>XAPO_FLAG_CHANNELS_MUST_MATCH</td>
<td>Channel count of the input and output streams must match.</td>
</tr>
<tr>
<td>XAPO_FLAG_FRAMERATE_MUST_MATCH</td>
<td>Framerate of input and output streams must match.</td>
</tr>
<tr>
<td>XAPO_FLAG_BITSPERSAMPLE_MUST_MATCH</td>
<td>Bit depth and container size of input and output streams must match.</td>
</tr>
<tr>
<td>XAPO_FLAG_BUFFERCOUNT_MUST_MATCH</td>
<td>Number of input and output buffers must match, applies to 
     			<a href="/windows/win32/api/xapo/ns-xapo-xapo_lockforprocess_parameters">XAPO_LOCKFORPROCESS_BUFFER_PARAMETERS</a>. When the XAPO_FLAG_BUFFERCOUNT_MUST_MATCH flag is set
            <b>XAPO_REGISTRATION_PROPERTIES</b>.<b>MinInputBufferCount</b> must equal
            <b>XAPO_REGISTRATION_PROPERTIES</b>.<b>MinOutputBufferCount</b> and
            <b>XAPO_REGISTRATION_PROPERTIES</b>.<b>MaxInputBufferCount</b> must equal
            <b>XAPO_REGISTRATION_PROPERTIES</b>.<b>MaxOutputBufferCount</b>.
				</td>
</tr>
<tr>
<td>XAPOBASE_DEFAULT_FLAG</td>
<td>XAPO_FLAG_CHANNELS_MUST_MATCH | XAPO_FLAG_FRAMERATE_MUST_MATCH | 
            XAPO_FLAG_BITSPERSAMPLE_MUST_MATCH | XAPO_FLAG_BUFFERCOUNT_MUST_MATCH | XAPO_FLAG_INPLACE_SUPPORTED
            </td>
</tr>
</table>

### -field MinInputBufferCount

Minimum number of input streams required for processing.

### -field MaxInputBufferCount

Maximum number of input streams required for processing.

<div class="alert"><b>Note</b>  <i>MaxInputBufferCount</i> is currently limited to a value of 1.</div>
<div> </div>

### -field MinOutputBufferCount

Minimum number of output streams required for processing.

### -field MaxOutputBufferCount

Maximum number of output streams required for processing. 

<div class="alert"><b>Note</b>  <i>MaxOutputBufferCount</i> is currently limited to a value of 1.</div>
<div> </div>

## -remarks

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)

## -see-also

<a href="/windows/desktop/xaudio2/structures">Structures</a>