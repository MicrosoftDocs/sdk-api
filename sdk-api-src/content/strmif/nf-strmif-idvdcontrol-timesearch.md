---
UID: NF:strmif.IDvdControl.TimeSearch
title: IDvdControl::TimeSearch (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Halts playback of the current chapter and starts playback from the specified time in the same media file.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","TimeSearch method","IDvdControl.TimeSearch","IDvdControl::TimeSearch","IDvdControlTimeSearch","TimeSearch","TimeSearch method [DirectShow]","TimeSearch method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_timesearch","strmif/IDvdControl::TimeSearch"]
old-location: dshow\idvdcontrol_timesearch.htm
tech.root: dshow
ms.assetid: c2e6848e-569e-44f0-b676-e22e4df07d8d
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],TimeSearch method, IDvdControl.TimeSearch, IDvdControl::TimeSearch, IDvdControlTimeSearch, TimeSearch, TimeSearch method [DirectShow], TimeSearch method [DirectShow],IDvdControl interface, dshow.idvdcontrol_timesearch, strmif/IDvdControl::TimeSearch
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
 - IDvdControl::TimeSearch
 - strmif/IDvdControl::TimeSearch
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
 - IDvdControl.TimeSearch
---

# IDvdControl::TimeSearch


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Halts playback of the current chapter and starts playback from the specified time in the same media file.

## -parameters

### -param bcdTime

Pointer to the [DVD_TIMECODE](/windows/desktop/api/strmif/ns-strmif-dvd_timecode) structure where DirectShow will start playback.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_Title. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>