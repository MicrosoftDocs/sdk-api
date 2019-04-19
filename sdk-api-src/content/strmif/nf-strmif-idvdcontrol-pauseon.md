---
UID: NF:strmif.IDvdControl.PauseOn
title: IDvdControl::PauseOn (strmif.h)
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Pauses the current media file playback.
old-location: dshow\idvdcontrol_pauseon.htm
tech.root: DirectShow
ms.assetid: d67a7a16-41f9-4718-a6ad-d48ba77fb1d4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],PauseOn method, IDvdControl.PauseOn, IDvdControl::PauseOn, IDvdControlPauseOn, PauseOn, PauseOn method [DirectShow], PauseOn method [DirectShow],IDvdControl interface, dshow.idvdcontrol_pauseon, strmif/IDvdControl::PauseOn
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
 - IDvdControl.PauseOn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::PauseOn


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Pauses the current media file playback.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method freezes playback and any internal timers, similar to <a href="https://msdn.microsoft.com/cfb875b7-cc4e-4ae2-8379-964d0e3ceb04">IMediaControl::Pause</a>. If the media file was not running, this method does nothing.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>



<a href="https://msdn.microsoft.com/6ec442dd-74ca-4b0b-901f-8efb7e77c5bf">IDvdControl::PauseOff</a>
 

 

