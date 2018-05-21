---
UID: NF:strmif.IDvdControl.GoUp
title: IDvdControl::GoUp
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current media file and starts playback of the designated previous program chain (PGC).
old-location: dshow\idvdcontrol_goup.htm
old-project: DirectShow
ms.assetid: 2a553a5f-f221-4161-95f1-cb1629abb87a
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GoUp, GoUp method [DirectShow], GoUp method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],GoUp method, IDvdControl.GoUp, IDvdControl::GoUp, IDvdControlGoUp, dshow.idvdcontrol_goup, strmif/IDvdControl::GoUp
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
-	IDvdControl.GoUp
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::GoUp


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current media file and starts playback of the designated previous program chain (PGC).




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Each PGC is associated with a previous PGC at authoring time, which this method sets as the new playback file.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

