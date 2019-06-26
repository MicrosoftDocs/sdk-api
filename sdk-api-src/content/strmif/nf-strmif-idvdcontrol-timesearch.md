---
UID: NF:strmif.IDvdControl.TimeSearch
title: IDvdControl::TimeSearch (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current chapter and starts playback from the specified time in the same media file.
old-location: dshow\idvdcontrol_timesearch.htm
tech.root: DirectShow
ms.assetid: c2e6848e-569e-44f0-b676-e22e4df07d8d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],TimeSearch method, IDvdControl.TimeSearch, IDvdControl::TimeSearch, IDvdControlTimeSearch, TimeSearch, TimeSearch method [DirectShow], TimeSearch method [DirectShow],IDvdControl interface, dshow.idvdcontrol_timesearch, strmif/IDvdControl::TimeSearch
ms.topic: method
f1_keywords: 
 - "strmif/IDvdControl.TimeSearch"
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
 - IDvdControl.TimeSearch
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::TimeSearch


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current chapter and starts playback from the specified time in the same media file.




## -parameters




### -param bcdTime

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-tagdvd_timecode">DVD_TIMECODE</a> structure where DirectShow will start playback.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-tagdvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

