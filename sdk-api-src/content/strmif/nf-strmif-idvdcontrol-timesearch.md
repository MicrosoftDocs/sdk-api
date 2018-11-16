---
UID: NF:strmif.IDvdControl.TimeSearch
title: IDvdControl::TimeSearch
author: windows-sdk-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current chapter and starts playback from the specified time in the same media file.
old-location: dshow\idvdcontrol_timesearch.htm
tech.root: DirectShow
ms.assetid: c2e6848e-569e-44f0-b676-e22e4df07d8d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDvdControl interface [DirectShow],TimeSearch method, IDvdControl.TimeSearch, IDvdControl::TimeSearch, IDvdControlTimeSearch, TimeSearch, TimeSearch method [DirectShow], TimeSearch method [DirectShow],IDvdControl interface, dshow.idvdcontrol_timesearch, strmif/IDvdControl::TimeSearch
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
 - IDvdControl.TimeSearch
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
- IDvdControl.TimeSearch
: 
---

# IDvdControl::TimeSearch


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current chapter and starts playback from the specified time in the same media file.




## -parameters




### -param bcdTime

Pointer to the <a href="https://msdn.microsoft.com/7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4">DVD_TIMECODE</a> structure where DirectShow will start playback.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

