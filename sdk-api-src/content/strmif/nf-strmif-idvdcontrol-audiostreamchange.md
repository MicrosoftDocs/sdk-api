---
UID: NF:strmif.IDvdControl.AudioStreamChange
title: IDvdControl::AudioStreamChange
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the current audio stream.
old-location: dshow\idvdcontrol_audiostreamchange.htm
tech.root: DirectShow
ms.assetid: 08fca00b-e187-40db-99c0-8b978dd0f10e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AudioStreamChange, AudioStreamChange method [DirectShow], AudioStreamChange method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],AudioStreamChange method, IDvdControl.AudioStreamChange, IDvdControl::AudioStreamChange, IDvdControlAudioStreamChange, dshow.idvdcontrol_audiostreamchange, strmif/IDvdControl::AudioStreamChange
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: 
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
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.AudioStreamChange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::AudioStreamChange


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the current audio stream.




## -parameters




### -param ulAudio [in]

Value that specifies the audio track to use, which must be from 0 through 7.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

<code>AudioStreamChange</code> affects the audio of the current Video Title Set (VTS). When called from within a menu, this method sets the audio stream of the title from which the menu was called.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

