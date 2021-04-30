---
UID: NF:audiomediatype.IAudioMediaType.IsEqual
title: IAudioMediaType::IsEqual (audiomediatype.h)
description: The IsEqual method compares two media types and determines whether they are identical.
helpviewer_keywords: ["IAudioMediaType interface [Audio Devices]","IsEqual method","IAudioMediaType.IsEqual","IAudioMediaType::IsEqual","IsEqual","IsEqual method [Audio Devices]","IsEqual method [Audio Devices]","IAudioMediaType interface","audio.iaudiomediatype_isequal","audio_syseffects_r_0b3614f0-18af-462e-9ab4-3e625bec54ab.xml","audiomediatype/IAudioMediaType::IsEqual"]
old-location: audio\iaudiomediatype_isequal.htm
tech.root: audio
ms.assetid: a8ab9ad3-251d-43ab-b099-793ffc22b45f
ms.date: 12/05/2018
ms.keywords: IAudioMediaType interface [Audio Devices],IsEqual method, IAudioMediaType.IsEqual, IAudioMediaType::IsEqual, IsEqual, IsEqual method [Audio Devices], IsEqual method [Audio Devices],IAudioMediaType interface, audio.iaudiomediatype_isequal, audio_syseffects_r_0b3614f0-18af-462e-9ab4-3e625bec54ab.xml, audiomediatype/IAudioMediaType::IsEqual
req.header: audiomediatype.h
req.include-header: Audiomediatype.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.irql: All levels.
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMediaType::IsEqual
 - audiomediatype/IAudioMediaType::IsEqual
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiomediatype.h
api_name:
 - IAudioMediaType.IsEqual
---

# IAudioMediaType::IsEqual


## -description

The <code>IsEqual</code> method compares two media types and determines whether they are identical.

## -parameters

### -param pIAudioType [in]

Specifies a pointer to an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> interface of the media type to compare.

### -param pdwFlags [out]

Specifies a pointer to a DWORD variable that contains the bitwise OR result of zero or more flags. These flags indicate the degree of similarity between the two media types. The following table shows the supported flags.

<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td>
AUDIOMEDIATYPE_EQUAL_FORMAT_TYPES

</td>
<td>
The audio format types are the same.

</td>
</tr>
<tr>
<td>
AUDIOMEDIATYPE_EQUAL_FORMAT_DATA

</td>
<td>
The format information matches, not including extra data beyond the base <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure.

</td>
</tr>
<tr>
<td>
AUDIOMEDIATYPE_EQUAL_FORMAT_USER_DATA

</td>
<td>
The extra data is identical, or neither media type contains extra data.

</td>
</tr>
</table>

## -returns

The <code>IsEqual</code> method returns S_OK if it is successful, otherwise it returns one of the HRESULT values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One media type is invalid or both media types are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The media types are not equal. Examine the <i>pdwFlags</i> parameter to determine how the media types differ.

</td>
</tr>
</table>

## -remarks

Both media types must have a major type, otherwise the method returns E_INVALIDARG. For more information about media types, see <a href="/previous-versions//aa390528(v=vs.85)">Media Types</a>.

The MF_MEDIATYPE_EQUAL_FORMAT_DATA flag indicates that both media types have compatible attributes, although one might be a superset of the other. This method of comparison means that you can compare a partially-specified media type against a complete media type. For example, you might have two video types that describe the same format, but one type includes attributes for extended color information (chroma siting, nominal range, and so forth).

If the method succeeds and all the comparison flags are set in <i>pdwFlags</i>, the return value is S_OK. If the method succeeds but some comparison flags are not set, the method returns S_FALSE.

## -see-also

<a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a>



<a href="/previous-versions//aa390528(v=vs.85)">Media Types</a>



<a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a>