---
UID: NF:audioenginebaseapo.IAudioSystemEffectsCustomFormats.GetFormatRepresentation
title: IAudioSystemEffectsCustomFormats::GetFormatRepresentation (audioenginebaseapo.h)
description: The GetFormatRepresentation method retrieves a string representation of the custom format so that it can be displayed on a user-interface.
helpviewer_keywords: ["GetFormatRepresentation","GetFormatRepresentation method [Audio Devices]","GetFormatRepresentation method [Audio Devices]","IAudioSystemEffectsCustomFormats interface","IAudioSystemEffectsCustomFormats interface [Audio Devices]","GetFormatRepresentation method","IAudioSystemEffectsCustomFormats.GetFormatRepresentation","IAudioSystemEffectsCustomFormats::GetFormatRepresentation","audio.iaudiosystemeffectscustomformats_getformatrepresentation","audio_syseffects_r_0164d130-f6cc-423b-9195-e5e87ee6bf2f.xml","audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormatRepresentation"]
old-location: audio\iaudiosystemeffectscustomformats_getformatrepresentation.htm
tech.root: audio
ms.assetid: 35953b82-8832-4e7b-9186-e336fdc65362
ms.date: 12/05/2018
ms.keywords: GetFormatRepresentation, GetFormatRepresentation method [Audio Devices], GetFormatRepresentation method [Audio Devices],IAudioSystemEffectsCustomFormats interface, IAudioSystemEffectsCustomFormats interface [Audio Devices],GetFormatRepresentation method, IAudioSystemEffectsCustomFormats.GetFormatRepresentation, IAudioSystemEffectsCustomFormats::GetFormatRepresentation, audio.iaudiosystemeffectscustomformats_getformatrepresentation, audio_syseffects_r_0164d130-f6cc-423b-9195-e5e87ee6bf2f.xml, audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormatRepresentation
req.header: audioenginebaseapo.h
req.include-header: Audioenginebaseapo.h
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
 - IAudioSystemEffectsCustomFormats::GetFormatRepresentation
 - audioenginebaseapo/IAudioSystemEffectsCustomFormats::GetFormatRepresentation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audioenginebaseapo.h
api_name:
 - IAudioSystemEffectsCustomFormats.GetFormatRepresentation
---

# IAudioSystemEffectsCustomFormats::GetFormatRepresentation


## -description

The <code>GetFormatRepresentation</code> method retrieves a string representation of the custom format so that it can be displayed on a user-interface.

## -parameters

### -param nFormat [in]

Specifies the index of a supported format. This parameter can be any value in the range from zero to one less than the return value of <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatcount">GetFormatCount</a>. In other words, any value in the range from zero to GetFormatCount( ) - 1.

### -param ppwstrFormatRep [out, optional]

Specifies the address of the buffer that receives a NULL-terminated Unicode string that describes the custom format.

## -returns

The <code>GetFormatRepresentation</code> method returns S_OK when the call is successful. Otherwise, it returns one of the error codes shown in the following table.

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
Invalid pointer passed to function

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Return buffer cannot be allocated

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
nFormat is out of range

</td>
</tr>
</table>

## -remarks

The sAPO uses <a href="/previous-versions/windows/embedded/ms886939(v=msdn.10)">CoTaskMemAlloc</a> to allocate the returned string. The caller must use <a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to delete the buffer that is pointed to by the <i>ppwstrFormatRep</i> parameter.

## -see-also

<a href="/previous-versions/windows/embedded/ms886939(v=msdn.10)">CoTaskMemAlloc</a>



<a href="/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformatcount">GetFormatCount</a>