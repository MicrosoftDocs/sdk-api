---
UID: NF:strmif.IDvdControl.PauseOn
title: IDvdControl::PauseOn (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Pauses the current media file playback.helpviewer_keywords: ["IDvdControl interface [DirectShow]","PauseOn method","IDvdControl.PauseOn","IDvdControl::PauseOn","IDvdControlPauseOn","PauseOn","PauseOn method [DirectShow]","PauseOn method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_pauseon","strmif/IDvdControl::PauseOn"]
old-location: dshow\idvdcontrol_pauseon.htm
tech.root: DirectShow
ms.assetid: d67a7a16-41f9-4718-a6ad-d48ba77fb1d4
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],PauseOn method, IDvdControl.PauseOn, IDvdControl::PauseOn, IDvdControlPauseOn, PauseOn, PauseOn method [DirectShow], PauseOn method [DirectShow],IDvdControl interface, dshow.idvdcontrol_pauseon, strmif/IDvdControl::PauseOn
f1_keywords:
- strmif/IDvdControl.PauseOn
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::PauseOn


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Pauses the current media file playback.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method freezes playback and any internal timers, similar to <a href="https://docs.microsoft.com/windows/desktop/api/control/nf-control-imediacontrol-pause">IMediaControl::Pause</a>. If the media file was not running, this method does nothing.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-pauseoff">IDvdControl::PauseOff</a>
 

 

