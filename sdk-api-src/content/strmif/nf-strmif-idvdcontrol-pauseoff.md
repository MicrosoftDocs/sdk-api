---
UID: NF:strmif.IDvdControl.PauseOff
title: IDvdControl::PauseOff
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Resumes playback of the current media file after a pause.
old-location: dshow\idvdcontrol_pauseoff.htm
tech.root: DirectShow
ms.assetid: 6ec442dd-74ca-4b0b-901f-8efb7e77c5bf
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IDvdControl interface [DirectShow],PauseOff method, IDvdControl.PauseOff, IDvdControl::PauseOff, IDvdControlPauseOff, PauseOff, PauseOff method [DirectShow], PauseOff method [DirectShow],IDvdControl interface, dshow.idvdcontrol_pauseoff, strmif/IDvdControl::PauseOff
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
 - IDvdControl.PauseOff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl::PauseOff


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Resumes playback of the current media file after a pause.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the media file was not paused in playback, this method does nothing.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>



<a href="https://msdn.microsoft.com/d67a7a16-41f9-4718-a6ad-d48ba77fb1d4">IDvdControl::PauseOn</a>
 

 

