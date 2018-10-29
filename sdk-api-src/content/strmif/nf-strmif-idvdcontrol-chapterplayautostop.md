---
UID: NF:strmif.IDvdControl.ChapterPlayAutoStop
title: IDvdControl::ChapterPlayAutoStop
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Instructs the DVD player to start playing at the specified chapter within the specified title and play the number of chapters specified.
old-location: dshow\idvdcontrol_chapterplayautostop.htm
tech.root: DirectShow
ms.assetid: 0c599647-c894-47b9-a62d-3ffd22843f7c
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ChapterPlayAutoStop, ChapterPlayAutoStop method [DirectShow], ChapterPlayAutoStop method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterPlayAutoStop method, IDvdControl.ChapterPlayAutoStop, IDvdControl::ChapterPlayAutoStop, IDvdControlChapterPlayAutoStop, dshow.idvdcontrol_chapterplayautostop, strmif/IDvdControl::ChapterPlayAutoStop
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
 - IDvdControl.ChapterPlayAutoStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::ChapterPlayAutoStop


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Instructs the DVD player to start playing at the specified chapter within the specified title and play the number of chapters specified.




## -parameters




### -param ulTitle [in]

Title number for playback.


### -param ulChapter [in]

Chapter number to start playback.


### -param ulChaptersToPlay [in]

Number of chapters to play from the start chapter.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method is valid in any domain. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.

Chapters range from 1 through 999. See EC_DVD_CHAPTER_AUTOSTOP in <a href="https://msdn.microsoft.com/c028918e-aba2-49b2-a6ce-c620ab38b558">DVD Event Notification Codes</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

