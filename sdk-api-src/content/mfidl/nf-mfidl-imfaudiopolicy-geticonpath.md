---
UID: NF:mfidl.IMFAudioPolicy.GetIconPath
title: IMFAudioPolicy::GetIconPath (mfidl.h)
description: Retrieves the icon resource for the audio session. The Windows volume control displays this icon.
helpviewer_keywords: ["GetIconPath","GetIconPath method [Media Foundation]","GetIconPath method [Media Foundation]","IMFAudioPolicy interface","IMFAudioPolicy interface [Media Foundation]","GetIconPath method","IMFAudioPolicy.GetIconPath","IMFAudioPolicy::GetIconPath","f2114f15-4357-4b5a-b384-695165d887de","mf.imfaudiopolicy_geticonpath","mfidl/IMFAudioPolicy::GetIconPath"]
old-location: mf\imfaudiopolicy_geticonpath.htm
tech.root: mf
ms.assetid: f2114f15-4357-4b5a-b384-695165d887de
ms.date: 12/05/2018
ms.keywords: GetIconPath, GetIconPath method [Media Foundation], GetIconPath method [Media Foundation],IMFAudioPolicy interface, IMFAudioPolicy interface [Media Foundation],GetIconPath method, IMFAudioPolicy.GetIconPath, IMFAudioPolicy::GetIconPath, f2114f15-4357-4b5a-b384-695165d887de, mf.imfaudiopolicy_geticonpath, mfidl/IMFAudioPolicy::GetIconPath
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFAudioPolicy::GetIconPath
 - mfidl/IMFAudioPolicy::GetIconPath
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFAudioPolicy.GetIconPath
---

# IMFAudioPolicy::GetIconPath


## -description

Retrieves the icon resource for the audio session. The Windows volume control displays this icon.

## -parameters

### -param pszPath [out]

Receives a pointer to a wide-character string that specifies a shell resource. The format of the string is described in the topic <a href="/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-seticonpath">IMFAudioPolicy::SetIconPath</a>. The caller must free the memory allocated for the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

If the application did not set an icon path, the method returns an empty string ("").

For more information, see <b>IAudioSessionControl::GetIconPath</b> in the core audio API documentation.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy">IMFAudioPolicy</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>