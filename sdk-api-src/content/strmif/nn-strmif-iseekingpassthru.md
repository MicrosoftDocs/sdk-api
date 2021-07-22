---
UID: NN:strmif.ISeekingPassThru
title: ISeekingPassThru (strmif.h)
description: The ISeekingPassThru interface creates a helper object that implements seeking for one-input filters.
helpviewer_keywords: ["ISeekingPassThru","ISeekingPassThru interface [DirectShow]","ISeekingPassThru interface [DirectShow]","described","ISeekingPassThruInterface","dshow.iseekingpassthru","strmif/ISeekingPassThru"]
old-location: dshow\iseekingpassthru.htm
tech.root: dshow
ms.assetid: a22f2723-b44e-4c7e-8508-db5c6af5b1d6
ms.date: 12/05/2018
ms.keywords: ISeekingPassThru, ISeekingPassThru interface [DirectShow], ISeekingPassThru interface [DirectShow],described, ISeekingPassThruInterface, dshow.iseekingpassthru, strmif/ISeekingPassThru
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
 - ISeekingPassThru
 - strmif/ISeekingPassThru
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
 - ISeekingPassThru
---

# ISeekingPassThru interface


## -description

The <code>ISeekingPassThru</code> interface creates a helper object that implements seeking for one-input filters. Filters can use this interface to implement the <a href="/windows/desktop/api/strmif/nn-strmif-imediaseeking">IMediaSeeking</a> and <a href="/windows/desktop/api/control/nn-control-imediaposition">IMediaPosition</a> interfaces. For more information, see <a href="/windows/desktop/DirectShow/cpospassthru">CPosPassThru</a>.

Applications do not use this interface.

## -inheritance

The <b>ISeekingPassThru</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISeekingPassThru</b> also has these types of members:

## -remarks

To obtain this interface, call <b>CoCreateInstance</b> with CLSID_SeekingPassThru. You can also use the <a href="/windows/desktop/DirectShow/createpospassthru">CreatePosPassThru</a> function in the base class library.
