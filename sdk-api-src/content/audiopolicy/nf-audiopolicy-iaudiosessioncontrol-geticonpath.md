---
UID: NF:audiopolicy.IAudioSessionControl.GetIconPath
title: IAudioSessionControl::GetIconPath (audiopolicy.h)
description: The GetIconPath method retrieves the path for the display icon for the audio session.
helpviewer_keywords: ["GetIconPath","GetIconPath method [Core Audio]","GetIconPath method [Core Audio]","IAudioSessionControl interface","IAudioSessionControl interface [Core Audio]","GetIconPath method","IAudioSessionControl.GetIconPath","IAudioSessionControl::GetIconPath","IAudioSessionControlGetIconPath","audiopolicy/IAudioSessionControl::GetIconPath","coreaudio.iaudiosessioncontrol_geticonpath"]
old-location: coreaudio\iaudiosessioncontrol_geticonpath.htm
tech.root: CoreAudio
ms.assetid: e5b2721a-fd0a-483d-a94c-6e1520f5764c
ms.date: 12/05/2018
ms.keywords: GetIconPath, GetIconPath method [Core Audio], GetIconPath method [Core Audio],IAudioSessionControl interface, IAudioSessionControl interface [Core Audio],GetIconPath method, IAudioSessionControl.GetIconPath, IAudioSessionControl::GetIconPath, IAudioSessionControlGetIconPath, audiopolicy/IAudioSessionControl::GetIconPath, coreaudio.iaudiosessioncontrol_geticonpath
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
 - IAudioSessionControl::GetIconPath
 - audiopolicy/IAudioSessionControl::GetIconPath
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
 - IAudioSessionControl.GetIconPath
---

# IAudioSessionControl::GetIconPath


## -description

The <b>GetIconPath</b> method retrieves the path for the display icon for the audio session.

## -parameters

### -param pRetVal [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string that specifies the fully qualified path of an .ico, .dll, or .exe file that contains the icon. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> function. For information about icon paths and <b>CoTaskMemFree</b>, see the Windows SDK documentation.

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

If a client has not called <a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-seticonpath">IAudioSessionControl::SetIconPath</a> to set the display icon, the string will be empty. If no client-specified icon is available, the Sndvol program uses the icon from the client's application window to label the volume control for the audio session.

## -see-also

<a href="/windows/desktop/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol">IAudioSessionControl Interface</a>



<a href="/windows/desktop/api/audiopolicy/nf-audiopolicy-iaudiosessioncontrol-seticonpath">IAudioSessionControl::SetIconPath</a>