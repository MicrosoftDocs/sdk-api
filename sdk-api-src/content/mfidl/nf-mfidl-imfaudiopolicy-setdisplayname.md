---
UID: NF:mfidl.IMFAudioPolicy.SetDisplayName
title: IMFAudioPolicy::SetDisplayName (mfidl.h)
description: Sets the display name of the audio session. The Windows volume control displays this name.
helpviewer_keywords: ["4cd48400-8d12-4a6b-95fd-bf6ae7700cb8","IMFAudioPolicy interface [Media Foundation]","SetDisplayName method","IMFAudioPolicy.SetDisplayName","IMFAudioPolicy::SetDisplayName","SetDisplayName","SetDisplayName method [Media Foundation]","SetDisplayName method [Media Foundation]","IMFAudioPolicy interface","mf.imfaudiopolicy_setdisplayname","mfidl/IMFAudioPolicy::SetDisplayName"]
old-location: mf\imfaudiopolicy_setdisplayname.htm
tech.root: mf
ms.assetid: 4cd48400-8d12-4a6b-95fd-bf6ae7700cb8
ms.date: 12/05/2018
ms.keywords: 4cd48400-8d12-4a6b-95fd-bf6ae7700cb8, IMFAudioPolicy interface [Media Foundation],SetDisplayName method, IMFAudioPolicy.SetDisplayName, IMFAudioPolicy::SetDisplayName, SetDisplayName, SetDisplayName method [Media Foundation], SetDisplayName method [Media Foundation],IMFAudioPolicy interface, mf.imfaudiopolicy_setdisplayname, mfidl/IMFAudioPolicy::SetDisplayName
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
 - IMFAudioPolicy::SetDisplayName
 - mfidl/IMFAudioPolicy::SetDisplayName
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
 - IMFAudioPolicy.SetDisplayName
---

# IMFAudioPolicy::SetDisplayName


## -description

Sets the display name of the audio session. The Windows volume control displays this name.

## -parameters

### -param pszName [in]

A null-terminated wide-character string that contains the display name.

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