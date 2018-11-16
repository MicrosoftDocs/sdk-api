---
UID: NF:strmif.IDvdControl2.SelectAudioStream
title: IDvdControl2::SelectAudioStream
author: windows-sdk-content
description: The SelectAudioStream method selects the audio stream to play.
old-location: dshow\idvdcontrol2_selectaudiostream.htm
tech.root: DirectShow
ms.assetid: 845d00d5-3698-4cf5-bae4-abb9529c3f88
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectAudioStream method, IDvdControl2.SelectAudioStream, IDvdControl2::SelectAudioStream, IDvdControl2SelectAudioStream, SelectAudioStream, SelectAudioStream method [DirectShow], SelectAudioStream method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectaudiostream, strmif/IDvdControl2::SelectAudioStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SelectAudioStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- strmif.h
: 
- IDvdControl2.SelectAudioStream
: 
---

# IDvdControl2::SelectAudioStream


## -description



The <code>SelectAudioStream</code> method selects the audio stream to play.




## -parameters




### -param ulAudio [in]

Value that specifies the audio stream. Valid stream numbers are 0 through 7, or <b>DVD_DEFAULT_AUDIO_STREAM</b> to specify the default stream.


### -param dwFlags [in]

Bitwise OR of one or more flags from the <a href="https://msdn.microsoft.com/05eb5ab8-a1b3-4876-bac3-29510af8cdbd">DVD_CMD_FLAGS</a> enumeration, specifying how to synchronize the command. This parameter is currently ignored; use DVD_CMD_FLAG_None.


### -param ppCmd [out]

Receives a pointer to an <a href="https://msdn.microsoft.com/85f9b208-ddc2-4d9c-a30b-b666c81a49d2">IDvdCmd</a> object that can be used to synchronize DVD commands. The caller must release the interface. This parameter can be <b>NULL</b>. For more information, see <a href="https://msdn.microsoft.com/37e8f940-617d-43f6-92bd-aadccafe0059">Synchronizing DVD Commands</a>.


## -returns



Returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No default audio stream was found; or <i>dwFlags</i> is not zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ulAudio</i> is out of range, or doesn't correspond to an audio stream.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulAudio</i> value is valid, but the DVD Navigator could not set it for some reason.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_STREAM_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
The specified stream is disabled.

</td>
</tr>
</table>
 




## -remarks



This method affects the audio of the current Video Title Set (VTS). When called from within a menu, this method sets the audio stream of the title from which the menu was called.

The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Audio_Stream_Change</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
<li>DVD_DOMAIN_Stop</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>
 

 

