---
UID: NF:strmif.IDvdControl.Resume
title: IDvdControl::Resume method
author: windows-driver-content
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Returns to playing back a title from a menu.
old-location: dshow\idvdcontrol_resume.htm
old-project: DirectShow
ms.assetid: 336908bb-369e-449d-a94a-dd22fa72f20a
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IDvdControl, IDvdControl interface [DirectShow], Resume method, IDvdControl::Resume, IDvdControlResume, Resume method [DirectShow], Resume method [DirectShow], IDvdControl interface, Resume,IDvdControl.Resume, dshow.idvdcontrol_resume, strmif/IDvdControl::Resume
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
-	IDvdControl.Resume
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDvdControl::Resume method


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2</a> instread.</div>
<div> </div>
Returns to playing back a title from a menu.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the file is stopped or already running, this method does nothing.

This method returns to title playback in DVD_DOMAIN_Title. Applications typically call this method after <a href="https://msdn.microsoft.com/b0e27b7a-cf14-4b4c-849e-0fa7f6b1c0ed">MenuCall</a> which puts the DVD Navigator in DVD_DOMAIN_VideoTitleSetMenu or DVD_DOMAIN_VideoManagerMenu.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu or DVD_DOMAIN_VideoTitleSetMenu. For more information, see <a href="https://msdn.microsoft.com/2763a159-d4de-44c2-905b-5828f328cbd2">DVD_DOMAIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a6ca0fe8-84e3-43e6-9421-29dcff056dfd">IDvdControl Interface</a>
 

 

