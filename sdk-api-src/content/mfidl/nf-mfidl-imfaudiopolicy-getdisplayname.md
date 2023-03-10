---
UID: NF:mfidl.IMFAudioPolicy.GetDisplayName
title: IMFAudioPolicy::GetDisplayName (mfidl.h)
description: Retrieves the display name of the audio session. The Windows volume control displays this name.
helpviewer_keywords: ["7826b4a1-5887-46a5-b312-91159596ccf5","GetDisplayName","GetDisplayName method [Media Foundation]","GetDisplayName method [Media Foundation]","IMFAudioPolicy interface","IMFAudioPolicy interface [Media Foundation]","GetDisplayName method","IMFAudioPolicy.GetDisplayName","IMFAudioPolicy::GetDisplayName","mf.imfaudiopolicy_getdisplayname","mfidl/IMFAudioPolicy::GetDisplayName"]
old-location: mf\imfaudiopolicy_getdisplayname.htm
tech.root: mf
ms.assetid: 7826b4a1-5887-46a5-b312-91159596ccf5
ms.date: 12/05/2018
ms.keywords: 7826b4a1-5887-46a5-b312-91159596ccf5, GetDisplayName, GetDisplayName method [Media Foundation], GetDisplayName method [Media Foundation],IMFAudioPolicy interface, IMFAudioPolicy interface [Media Foundation],GetDisplayName method, IMFAudioPolicy.GetDisplayName, IMFAudioPolicy::GetDisplayName, mf.imfaudiopolicy_getdisplayname, mfidl/IMFAudioPolicy::GetDisplayName
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
 - IMFAudioPolicy::GetDisplayName
 - mfidl/IMFAudioPolicy::GetDisplayName
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
 - IMFAudioPolicy.GetDisplayName
---

# IMFAudioPolicy::GetDisplayName


## -description

Retrieves the display name of the audio session. The Windows volume control displays this name.

## -parameters

### -param pszName [out]

Receives a pointer to the display name string. The caller must free the memory allocated for the string by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

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

If the application does not set a display name, Windows creates one.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy">IMFAudioPolicy</a>



<a href="/windows/desktop/medfound/streaming-audio-renderer">Streaming Audio Renderer</a>