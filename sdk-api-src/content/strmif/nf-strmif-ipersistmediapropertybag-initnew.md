---
UID: NF:strmif.IPersistMediaPropertyBag.InitNew
title: IPersistMediaPropertyBag::InitNew (strmif.h)
description: The InitNew method initializes the object to receive new properties.
helpviewer_keywords: ["IPersistMediaPropertyBag interface [DirectShow]","InitNew method","IPersistMediaPropertyBag.InitNew","IPersistMediaPropertyBag::InitNew","IPersistMediaPropertyBagInitNew","InitNew","InitNew method [DirectShow]","InitNew method [DirectShow]","IPersistMediaPropertyBag interface","dshow.ipersistmediapropertybag_initnew","strmif/IPersistMediaPropertyBag::InitNew"]
old-location: dshow\ipersistmediapropertybag_initnew.htm
tech.root: dshow
ms.assetid: 46d51c05-b653-4f14-810a-eb49d33da359
ms.date: 12/05/2018
ms.keywords: IPersistMediaPropertyBag interface [DirectShow],InitNew method, IPersistMediaPropertyBag.InitNew, IPersistMediaPropertyBag::InitNew, IPersistMediaPropertyBagInitNew, InitNew, InitNew method [DirectShow], InitNew method [DirectShow],IPersistMediaPropertyBag interface, dshow.ipersistmediapropertybag_initnew, strmif/IPersistMediaPropertyBag::InitNew
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IPersistMediaPropertyBag::InitNew
 - strmif/IPersistMediaPropertyBag::InitNew
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
 - IPersistMediaPropertyBag.InitNew
---

# IPersistMediaPropertyBag::InitNew


## -description

The <code>InitNew</code> method initializes the object to receive new properties.



## -returns

Returns S_OK.

## -remarks

Calling this method on the <a href="/windows/desktop/DirectShow/avi-mux-filter">AVI Mux</a> filter clears any properties that were previously set using the <a href="/windows/desktop/api/strmif/nf-strmif-ipersistmediapropertybag-load">Load</a> method.

Calling this method on the <a href="/windows/desktop/DirectShow/avi-splitter-filter">AVI Splitter</a> filter or the <a href="/windows/desktop/DirectShow/wave-parser-filter">WAVE Parser</a> filter has no effect.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ipersistmediapropertybag">IPersistMediaPropertyBag Interface</a>
