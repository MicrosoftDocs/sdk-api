---
UID: NF:strmif.IDvdControl.ChapterPlayAutoStop
title: IDvdControl::ChapterPlayAutoStop (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Instructs the DVD player to start playing at the specified chapter within the specified title and play the number of chapters specified.
old-location: dshow\idvdcontrol_chapterplayautostop.htm
tech.root: DirectShow
ms.assetid: 0c599647-c894-47b9-a62d-3ffd22843f7c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ChapterPlayAutoStop, ChapterPlayAutoStop method [DirectShow], ChapterPlayAutoStop method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterPlayAutoStop method, IDvdControl.ChapterPlayAutoStop, IDvdControl::ChapterPlayAutoStop, IDvdControlChapterPlayAutoStop, dshow.idvdcontrol_chapterplayautostop, strmif/IDvdControl::ChapterPlayAutoStop
ms.topic: method
f1_keywords: 
 - "strmif/IDvdControl.ChapterPlayAutoStop"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::ChapterPlayAutoStop


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
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



This method is valid in any domain. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

Chapters range from 1 through 999. See EC_DVD_CHAPTER_AUTOSTOP in <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-notification-codes">DVD Event Notification Codes</a> for more information.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

