---
UID: NF:strmif.IDvdControl.StopForResume
title: IDvdControl::StopForResume
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.
old-location: dshow\idvdcontrol_stopforresume.htm
old-project: DirectShow
ms.assetid: 61c5b863-038b-4c4a-a7a4-d1fd1801f843
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IDvdControl interface [DirectShow],StopForResume method, IDvdControl.StopForResume, IDvdControl::StopForResume, IDvdControlStopForResume, StopForResume, StopForResume method [DirectShow], StopForResume method [DirectShow],IDvdControl interface, dshow.idvdcontrol_stopforresume, strmif/IDvdControl::StopForResume
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::StopForResume


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Transitions playback to the DVD_DOMAIN_Stop state after saving resume information.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If no file is playing or paused, this method does nothing.

The <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter transfers to the stopped state, but the filter graph remains in the DirectShow run state.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

