---
UID: NF:strmif.IDvdControl.Resume
title: IDvdControl::Resume (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Returns to playing back a title from a menu.
old-location: dshow\idvdcontrol_resume.htm
tech.root: DirectShow
ms.assetid: 336908bb-369e-449d-a94a-dd22fa72f20a
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],Resume method, IDvdControl.Resume, IDvdControl::Resume, IDvdControlResume, Resume, Resume method [DirectShow], Resume method [DirectShow],IDvdControl interface, dshow.idvdcontrol_resume, strmif/IDvdControl::Resume
f1_keywords:
- strmif/IDvdControl.Resume
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
- IDvdControl.Resume
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvdControl::Resume


## -description



<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Returns to playing back a title from a menu.




## -parameters






## -returns



Returns an <b>HRESULT</b> value.




## -remarks



If the file is stopped or already running, this method does nothing.

This method returns to title playback in DVD_DOMAIN_Title. Applications typically call this method after <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdcontrol-menucall">MenuCall</a> which puts the DVD Navigator in DVD_DOMAIN_VideoTitleSetMenu or DVD_DOMAIN_VideoManagerMenu.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu or DVD_DOMAIN_VideoTitleSetMenu. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
 

 

