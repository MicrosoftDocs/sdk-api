---
UID: NF:strmif.IDvdControl.TimePlay
title: IDvdControl::TimePlay method
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Plays the media file with the specified title index, starting at the specified time.
old-location: dshow\idvdcontrol_timeplay.htm
old-project: DirectShow
ms.assetid: 56b4b086-e315-486c-8dbd-97960f5b76d1
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], TimePlay method, IDvdControl::TimePlay, IDvdControlTimePlay, TimePlay method [DirectShow], TimePlay method [DirectShow], IDvdControl interface, TimePlay,IDvdControl.TimePlay, dshow.idvdcontrol_timeplay, strmif/IDvdControl::TimePlay
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmif.h
api_name:
-	IDvdControl.TimePlay
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::TimePlay method


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Plays the media file with the specified title index, starting at the specified time.




## -parameters




### -param ulTitle




### -param bcdTime

Pointer to the <a href="https://msdn.microsoft.com/7ad0b11e-5bb7-426f-9a2c-fbc34b2f45b4">DVD_TIMECODE</a> structure where DirectShow will start playback.


#### - uiTitle

Value that specifies the title number DirectShow will play back; this value must be from 1 through 99.


## -returns



Returns an <b>HRESULT</b> value .




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

