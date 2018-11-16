---
UID: NF:strmif.IDvdControl.ChapterPlay
title: IDvdControl::ChapterPlay
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Plays the media file with the specified title index and chapter value.
old-location: dshow\idvdcontrol_chapterplay.htm
tech.root: DirectShow
ms.assetid: c51524d0-5935-4e14-bcaf-4739fd0f21bb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ChapterPlay, ChapterPlay method [DirectShow], ChapterPlay method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterPlay method, IDvdControl.ChapterPlay, IDvdControl::ChapterPlay, IDvdControlChapterPlay, dshow.idvdcontrol_chapterplay, strmif/IDvdControl::ChapterPlay
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
 - IDvdControl.ChapterPlay
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
- IDvdControl.ChapterPlay
: 
---

# IDvdControl::ChapterPlay


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Plays the media file with the specified title index and chapter value.




## -parameters




### -param ulTitle [in]

Value that specifies the title number DirectShow will play back; this value must be from 1 through 99.


### -param ulChapter [in]

Value that specifies the chapter within the specified title where DirectShow will start playback; this value must be from 1 through 999.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

