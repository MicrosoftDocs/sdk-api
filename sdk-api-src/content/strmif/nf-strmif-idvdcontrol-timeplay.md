---
UID: NF:strmif.IDvdControl.TimePlay
title: IDvdControl::TimePlay (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Plays the media file with the specified title index, starting at the specified time.
old-location: dshow\idvdcontrol_timeplay.htm
tech.root: DirectShow
ms.assetid: 56b4b086-e315-486c-8dbd-97960f5b76d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],TimePlay method, IDvdControl.TimePlay, IDvdControl::TimePlay, IDvdControlTimePlay, TimePlay, TimePlay method [DirectShow], TimePlay method [DirectShow],IDvdControl interface, dshow.idvdcontrol_timeplay, strmif/IDvdControl::TimePlay
ms.topic: method
f1_keywords: 
 - "strmif/IDvdControl.TimePlay"
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
 - IDvdControl.TimePlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::TimePlay


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Plays the media file with the specified title index, starting at the specified time.




## -parameters




### -param ulTitle

Value that specifies the title number DirectShow will play back; this value must be from 1 through 99.


### -param bcdTime

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ns-strmif-dvd_timecode">DVD_TIMECODE</a> structure where DirectShow will start playback.


## -returns



Returns an <b>HRESULT</b> value .




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

