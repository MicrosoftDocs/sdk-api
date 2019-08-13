---
UID: NF:strmif.IDvdControl.StopForResume
title: IDvdControl::StopForResume (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.
old-location: dshow\idvdcontrol_stopforresume.htm
tech.root: DirectShow
ms.assetid: 61c5b863-038b-4c4a-a7a4-d1fd1801f843
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],StopForResume method, IDvdControl.StopForResume, IDvdControl::StopForResume, IDvdControlStopForResume, StopForResume, StopForResume method [DirectShow], StopForResume method [DirectShow],IDvdControl interface, dshow.idvdcontrol_stopforresume, strmif/IDvdControl::StopForResume
ms.topic: method
f1_keywords: 
 - "strmif/IDvdControl.StopForResume"
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
 - IDvdControl.StopForResume
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::StopForResume


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If no file is playing or paused, this method does nothing.

The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter transfers to the stopped state, but the filter graph remains in the DirectShow run state.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

