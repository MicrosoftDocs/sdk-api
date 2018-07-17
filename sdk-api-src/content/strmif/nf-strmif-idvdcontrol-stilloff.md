---
UID: NF:strmif.IDvdControl.StillOff
title: IDvdControl::StillOff
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Resumes playback, canceling still mode.
old-location: dshow\idvdcontrol_stilloff.htm
old-project: DirectShow
ms.assetid: 0f466728-027e-40d6-b8f8-ed0aad02dd1e
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IDvdControl interface [DirectShow],StillOff method, IDvdControl.StillOff, IDvdControl::StillOff, IDvdControlStillOff, StillOff, StillOff method [DirectShow], StillOff method [DirectShow],IDvdControl interface, dshow.idvdcontrol_stilloff, strmif/IDvdControl::StillOff
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
 - IDvdControl.StillOff
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::StillOff


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Resumes playback, canceling still mode.




## -parameters






## -returns



Returns an <b>HRESULT</b> value .




## -remarks



If the display image was not in still-store mode, this method does nothing.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

