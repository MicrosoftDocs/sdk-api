---
UID: NF:strmif.IDvdControl.ForwardScan
title: IDvdControl::ForwardScan (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Searches forward through the current disc at the specified speed.
helpviewer_keywords: ["ForwardScan","ForwardScan method [DirectShow]","ForwardScan method [DirectShow]","IDvdControl interface","IDvdControl interface [DirectShow]","ForwardScan method","IDvdControl.ForwardScan","IDvdControl::ForwardScan","IDvdControlForwardScan","dshow.idvdcontrol_forwardscan","strmif/IDvdControl::ForwardScan"]
old-location: dshow\idvdcontrol_forwardscan.htm
tech.root: dshow
ms.assetid: dedeec1c-8565-491e-ab2c-4cdc17d988a9
ms.date: 12/05/2018
ms.keywords: ForwardScan, ForwardScan method [DirectShow], ForwardScan method [DirectShow],IDvdControl interface, IDvdControl interface [DirectShow],ForwardScan method, IDvdControl.ForwardScan, IDvdControl::ForwardScan, IDvdControlForwardScan, dshow.idvdcontrol_forwardscan, strmif/IDvdControl::ForwardScan
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
 - IDvdControl::ForwardScan
 - strmif/IDvdControl::ForwardScan
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
 - IDvdControl.ForwardScan
---

# IDvdControl::ForwardScan


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Searches forward through the current disc at the specified speed.

## -parameters

### -param dwSpeed [in]

Value that specifies how quickly DirectShow will search through the media file. This value is a multiplier, where 1.0 is the authored speed, so a value of 2.5 will search forward at two and one-half times the authored speed, while a value of 0.5 will search forward at half the authored speed. Note that the actual speed of playback depends on the capabilities of the video decoder, and might differ from the specified rate.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, or DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>