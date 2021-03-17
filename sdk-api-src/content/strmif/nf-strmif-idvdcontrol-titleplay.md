---
UID: NF:strmif.IDvdControl.TitlePlay
title: IDvdControl::TitlePlay (strmif.h)
description: Note  The IDvdControl interface is deprecated. Use IDvdControl2 instread. Finds the media file with the specified title index and plays it back.
helpviewer_keywords: ["IDvdControl interface [DirectShow]","TitlePlay method","IDvdControl.TitlePlay","IDvdControl::TitlePlay","IDvdControlTitlePlay","TitlePlay","TitlePlay method [DirectShow]","TitlePlay method [DirectShow]","IDvdControl interface","dshow.idvdcontrol_titleplay","strmif/IDvdControl::TitlePlay"]
old-location: dshow\idvdcontrol_titleplay.htm
tech.root: dshow
ms.assetid: 5ca710f0-8f08-43d6-8cc1-a25068d5e0ef
ms.date: 12/05/2018
ms.keywords: IDvdControl interface [DirectShow],TitlePlay method, IDvdControl.TitlePlay, IDvdControl::TitlePlay, IDvdControlTitlePlay, TitlePlay, TitlePlay method [DirectShow], TitlePlay method [DirectShow],IDvdControl interface, dshow.idvdcontrol_titleplay, strmif/IDvdControl::TitlePlay
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
 - IDvdControl::TitlePlay
 - strmif/IDvdControl::TitlePlay
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
 - IDvdControl.TitlePlay
---

# IDvdControl::TitlePlay


## -description

<div class="alert"><b>Note</b>  The <b>IDvdControl</b> interface is deprecated. Use <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> instread.</div>
<div> </div>
Finds the media file with the specified title index and plays it back.

## -parameters

### -param ulTitle

Value that specifies the title number DirectShow will play back; this value must be from 1 through 99.

## -returns

Returns an <b>HRESULT</b> value .

## -remarks

This method returns an error unless the domain is DVD_DOMAIN_VideoManagerMenu, DVD_DOMAIN_VideoTitleSetMenu, DVD_DOMAIN_Title, or DVD_DOMAIN_Stop. For more information, see <a href="/windows/desktop/api/strmif/ne-strmif-dvd_domain">DVD_DOMAIN</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol">IDvdControl Interface</a>