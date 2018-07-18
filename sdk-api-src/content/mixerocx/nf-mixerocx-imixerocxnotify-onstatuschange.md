---
UID: NF:mixerocx.IMixerOCXNotify.OnStatusChange
title: IMixerOCXNotify::OnStatusChange
author: windows-sdk-content
description: The OnStatusChange method informs the client that a status change has occurred.
old-location: dshow\imixerocxnotify_onstatuschange.htm
old-project: DirectShow
ms.assetid: b6e49306-59bc-45a2-826b-cea2cf77214b
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IMixerOCXNotify interface [DirectShow],OnStatusChange method, IMixerOCXNotify.OnStatusChange, IMixerOCXNotify::OnStatusChange, IMixerOCXNotifyOnStatusChange, OnStatusChange, OnStatusChange method [DirectShow], OnStatusChange method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_onstatuschange, mixerocx/IMixerOCXNotify::OnStatusChange
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mixerocx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerOCXNotify.OnStatusChange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerOCXNotify::OnStatusChange


## -description



The <code>OnStatusChange</code> method informs the client that a status change has occurred.




## -parameters




### -param ulStatusFlags [in]

Bitwise OR of one or more of the following status flags.

<table>
<tr>
<th>
                  Flag
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MIXER_STATE_UNCONNECTED (0x00000000)</td>
<td>The Overlay Mixer is unconnected and stopped.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_STOPPED (0x00000001)</td>
<td>The Overlay Mixer is connected and stopped.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_PAUSED (0x00000002)</td>
<td>The Overlay Mixer is connected and paused.</td>
</tr>
<tr>
<td>MIXER_STATE_CONNECTED_PLAYING (0x00000003)</td>
<td>The Overlay Mixer is connected and playing.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/b73416c0-2312-4164-8a6d-f8776dc1447f">IMixerOCXNotify Interface</a>



<a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer</a>
 

 

