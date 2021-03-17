---
UID: NF:audiopolicy.IAudioSessionControl.GetDisplayName
title: IAudioSessionControl::GetDisplayName (audiopolicy.h)
description: The GetDisplayName method retrieves the display name for the audio session.
helpviewer_keywords: ["GetDisplayName","GetDisplayName method [Core Audio]","GetDisplayName method [Core Audio]","IAudioSessionControl interface","IAudioSessionControl interface [Core Audio]","GetDisplayName method","IAudioSessionControl.GetDisplayName","IAudioSessionControl::GetDisplayName","IAudioSessionControlGetDisplayName","audiopolicy/IAudioSessionControl::GetDisplayName","coreaudio.iaudiosessioncontrol_getdisplayname"]
old-location: coreaudio\iaudiosessioncontrol_getdisplayname.htm
tech.root: CoreAudio
ms.assetid: 28493e3a-ee5a-4331-b5b5-ba0bf2ee3370
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Core Audio], GetDisplayName method [Core Audio],IAudioSessionControl interface, IAudioSessionControl interface [Core Audio],GetDisplayName method, IAudioSessionControl.GetDisplayName, IAudioSessionControl::GetDisplayName, IAudioSessionControlGetDisplayName, audiopolicy/IAudioSessionControl::GetDisplayName, coreaudio.iaudiosessioncontrol_getdisplayname
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IAudioSessionControl::GetDisplayName
 - audiopolicy/IAudioSessionControl::GetDisplayName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiopolicy.h
api_name:
 - IAudioSessionControl.GetDisplayName
---

# IAudioSessionControl::GetDisplayName


## -description

The <b>GetDisplayName</b> method retrieves the display name for the audio session.

## -parameters

### -param pRetVal [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that contains the display name. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.

## -returns

If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
Parameter <i>pRetVal</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>

## -remarks

If the client has not called <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a> to set the display name, the string will be empty. Rather than display an empty name string, the Sndvol program uses a default, automatically generated name to label the volume control for the audio session.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setdisplayname">IAudioSessionControl::SetDisplayName</a>