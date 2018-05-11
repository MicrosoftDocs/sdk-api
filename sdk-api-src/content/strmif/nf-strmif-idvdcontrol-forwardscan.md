---
UID: NF:strmif.IDvdControl.ForwardScan
title: IDvdControl::ForwardScan
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Searches forward through the current disc at the specified speed.
old-location: dshow\idvdcontrol_forwardscan.htm
old-project: DirectShow
ms.assetid: dedeec1c-8565-491e-ab2c-4cdc17d988a9
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ForwardScan, ForwardScan method [DirectShow], ForwardScan method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ForwardScan method, IDvdControl.ForwardScan, IDvdControl::ForwardScan, IDvdControlForwardScan, dshow.idvdcontrol_forwardscan, strmif/IDvdControl::ForwardScan
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
-	IDvdControl.ForwardScan
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::ForwardScan


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Searches forward through the current disc at the specified speed.




## -parameters




### -param dwSpeed [in]

Value that specifies how quickly DirectShow will search through the media file. This value is a multiplier, where 1.0 is the authored speed, so a value of 2.5 will search forward at two and one-half times the authored speed, while a value of 0.5 will search forward at half the authored speed. Note that the actual speed of playback depends on the capabilities of the video decoder, and might differ from the specified rate.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

