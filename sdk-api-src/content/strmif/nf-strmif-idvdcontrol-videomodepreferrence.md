---
UID: NF:strmif.IDvdControl.VideoModePreferrence
title: IDvdControl::VideoModePreferrence method
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Sets the video display mode the user prefers.
old-location: dshow\idvdcontrol_videomodepreferrence.htm
old-project: DirectShow
ms.assetid: 9e68b09c-534c-46d2-bda0-72f3d1d86b66
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], VideoModePreferrence method, IDvdControl::VideoModePreferrence, IDvdControlVideoModePreferrence, VideoModePreferrence method [DirectShow], VideoModePreferrence method [DirectShow], IDvdControl interface, VideoModePreferrence,IDvdControl.VideoModePreferrence, dshow.idvdcontrol_videomodepreferrence, strmif/IDvdControl::VideoModePreferrence
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
-	IDvdControl.VideoModePreferrence
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::VideoModePreferrence method


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Sets the video display mode the user prefers.




## -parameters




### -param ulPreferredDisplayMode [in]

Value that specifies the new display mode for DVD content. Member of the <a href="https://msdn.microsoft.com/afb235ae-ba60-491f-8b88-7fe824f00f77">DVD_PREFERRED_DISPLAY_MODE</a> enumerated data type.


## -returns



Returns an <b>HRESULT</b> value .




## -remarks



This method changes the default video window's aspect ratio, and can also specify a default aspect ratio conversion mechanism.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

