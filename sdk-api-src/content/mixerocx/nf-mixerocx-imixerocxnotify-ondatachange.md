---
UID: NF:mixerocx.IMixerOCXNotify.OnDataChange
title: IMixerOCXNotify::OnDataChange
author: windows-driver-content
description: The OnDataChange method notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.
old-location: dshow\imixerocxnotify_ondatachange.htm
old-project: DirectShow
ms.assetid: d8080e5f-99e7-47eb-96ff-53c4ed8d2ff1
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IMixerOCXNotify interface [DirectShow],OnDataChange method, IMixerOCXNotify.OnDataChange, IMixerOCXNotify::OnDataChange, IMixerOCXNotifyOnDataChange, OnDataChange, OnDataChange method [DirectShow], OnDataChange method [DirectShow],IMixerOCXNotify interface, dshow.imixerocxnotify_ondatachange, mixerocx/IMixerOCXNotify::OnDataChange
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WIN32_FIND_DATAW, *PWIN32_FIND_DATAW, *LPWIN32_FIND_DATAW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IMixerOCXNotify.OnDataChange
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMixerOCXNotify::OnDataChange


## -description



The <code>OnDataChange</code> method notifies the client when the video rectangle's aspect ratio or size, or the display palette, has changed.




## -parameters




### -param ulDataFlags [in]

Flag indicating which set of data has changed. The following flags are defined.

<table>
<tr>
<th>
                  Flags
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>MIXER_DATA_ASPECT_RATIO (0x00000001)</td>
<td>Picture aspect ratio.</td>
</tr>
<tr>
<td>MIXER_DATA_NATIVE_SIZE (0x00000002)</td>
<td>The video stream's native size changed.</td>
</tr>
<tr>
<td>MIXER_DATA_PALETTE (0x00000004)</td>
<td>The video palette changed.</td>
</tr>
</table>
 


## -returns



If the method succeeds, it returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/b80d720d-921d-4d24-a168-49944cfcc411">IMixerOCX Interface</a>



<a href="https://msdn.microsoft.com/b73416c0-2312-4164-8a6d-f8776dc1447f">IMixerOCXNotify Interface</a>
 

 

