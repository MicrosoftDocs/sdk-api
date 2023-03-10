---
UID: NF:strmif.IDvdControl.StillOff
title: IDvdControl::StillOff (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Resumes playback, canceling still mode.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","StillOff method","IDvdControl.StillOff","IDvdControl::StillOff","IDvdControlStillOff","StillOff","StillOff method [DirectShow]","StillOff method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_stilloff","strmif/IDvdControl::StillOff"]
old-location: dshow\idvdcontrol_stilloff.htm
tech.root: dshow
ms.assetid: 0f466728-027e-40d6-b8f8-ed0aad02dd1e
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],StillOff method, IDvdControl.StillOff, IDvdControl::StillOff, IDvdControlStillOff, StillOff, StillOff method [DirectShow], StillOff method [DirectShow],IDvdControl interface, dshow.idvdcontrol_stilloff, strmif/IDvdControl::StillOff
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdControl::StillOff
 - strmif/IDvdControl::StillOff
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IDvdControl.StillOff
---

# IDvdControl::StillOff


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Resumes playback, canceling still mode.



## -returns

Returns an <b>HRESULT</b> value .

## -remarks

If the display image was not in still-store mode, this method does nothing.

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>
