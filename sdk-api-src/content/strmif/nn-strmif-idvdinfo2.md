---
UID: NN:strmif.IDvdInfo2
title: IDvdInfo2 (strmif.h)
description: The IDvdInfo2 interface reports attributes of a DVD disc or the current state of DVD playback and navigation.
helpviewer_keywords: ["IDvdInfo2","IDvdInfo2 interface [DirectShow]","IDvdInfo2 interface [DirectShow]","described","IDvdInfo2Interface","dshow.idvdinfo2","strmif/IDvdInfo2"]
old-location: dshow\idvdinfo2.htm
tech.root: dshow
ms.assetid: da30d3dc-feec-4f54-b2db-a771ce404286
ms.date: 12/05/2018
ms.keywords: IDvdInfo2, IDvdInfo2 interface [DirectShow], IDvdInfo2 interface [DirectShow],described, IDvdInfo2Interface, dshow.idvdinfo2, strmif/IDvdInfo2
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvdInfo2
 - strmif/IDvdInfo2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdInfo2
---

# IDvdInfo2 interface


## -description

The <code>IDvdInfo2</code> interface reports attributes of a DVD disc or the current state of DVD playback and navigation. The <a href="/windows/desktop/DirectShow/dvd-navigator-filter">DVD Navigator</a> filter implements this interface. <code>IDvdInfo2</code> is the companion interface to <a href="/windows/desktop/api/strmif/nn-strmif-idvdcontrol2">IDvdControl2</a> interface. <code>IDvdInfo2</code> groups the DVD Navigator's "get" methods and <b>IDvdControl2</b> groups the "set" methods. Together they provide DVD navigation and playback functionality beyond the DVD Annex J specification.

<div class="alert"><b>Note</b>  The information provided by some of these methods can also be obtained through event notifications sent from the DVD Navigator to the application's message loop. For example, to get the current DVD domain, you can call <a href="/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getcurrentdomain">IDvdInfo2::GetCurrentDomain</a> or you can handle the <a href="/windows/desktop/DirectShow/ec-dvd-domain-change">EC_DVD_DOMAIN_CHANGE</a> event in your application's message loop and extract the new domain from the event's <i>lParam1</i> parameter.</div>
<div> </div>

## -inheritance

The <b>IDvdInfo2</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvdInfo2</b> also has these types of members:

## -see-also

<a href="/windows/desktop/DirectShow/dvd-applications">DVD Applications</a>
