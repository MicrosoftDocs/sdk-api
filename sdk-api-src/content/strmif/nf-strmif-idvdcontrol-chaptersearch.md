---
UID: NF:strmif.IDvdControl.ChapterSearch
title: IDvdControl::ChapterSearch (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current chapter and starts playback from the specified chapter within the same title.
old-location: dshow\idvdcontrol_chaptersearch.htm
tech.root: DirectShow
ms.assetid: 1389df65-e269-4c2b-b276-a29da33fe515
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ChapterSearch, ChapterSearch method [DirectShow], ChapterSearch method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ChapterSearch method, IDvdControl.ChapterSearch, IDvdControl::ChapterSearch, IDvdControlChapterSearch, dshow.idvdcontrol_chaptersearch, strmif/IDvdControl::ChapterSearch
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
 - IDvdControl.ChapterSearch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::ChapterSearch


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current chapter and starts playback from the specified chapter within the same title.




## -parameters




### -param ulChapter

Chapter value that specifies the point where playback will begin.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

