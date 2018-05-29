---
UID: NF:audiopolicy.IAudioSessionControl2.IsSystemSoundsSession
title: IAudioSessionControl2::IsSystemSoundsSession
author: windows-sdk-content
description: The IsSystemSoundsSession method indicates whether the session is a system sounds session.
old-location: coreaudio\iaudiosessioncontrol2_issystemsoundssession.htm
old-project: CoreAudio
ms.assetid: 9060f89c-83b1-433d-96e3-86ae4b1c7e7c
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAudioSessionControl2 interface [Core Audio],IsSystemSoundsSession method, IAudioSessionControl2.IsSystemSoundsSession, IAudioSessionControl2::IsSystemSoundsSession, IsSystemSoundsSession, IsSystemSoundsSession method [Core Audio], IsSystemSoundsSession method [Core Audio],IAudioSessionControl2 interface, audiopolicy/IAudioSessionControl2::IsSystemSoundsSession, coreaudio.iaudiosessioncontrol2_issystemsoundssession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: audiopolicy.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: UNCOMPRESSEDAUDIOFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	audiopolicy.h
api_name:
-	IAudioSessionControl2.IsSystemSoundsSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioSessionControl2::IsSystemSoundsSession


## -description


The <b>IsSystemSoundsSession</b> method indicates whether the session is a system sounds session.


## -parameters






## -returns




          The possible return codes include, but are not limited to, the values shown in the following table.

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
The session is a system sounds session.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The session is not a system sounds session.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3bb65edf-103c-4eeb-82b4-7c571cddfcf3">IAudioSessionControl2</a>
 

 

