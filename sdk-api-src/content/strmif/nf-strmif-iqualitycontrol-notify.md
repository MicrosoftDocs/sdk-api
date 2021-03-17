---
UID: NF:strmif.IQualityControl.Notify
title: IQualityControl::Notify (strmif.h)
description: The Notify method notifies the filter that a quality change is requested.
helpviewer_keywords: ["IQualityControl interface [DirectShow]","Notify method","IQualityControl.Notify","IQualityControl::Notify","IQualityControlNotify","Notify","Notify method [DirectShow]","Notify method [DirectShow]","IQualityControl interface","dshow.iqualitycontrol_notify","strmif/IQualityControl::Notify"]
old-location: dshow\iqualitycontrol_notify.htm
tech.root: dshow
ms.assetid: c7a34356-b0b2-49c1-bdc2-d8043fdc2862
ms.date: 12/05/2018
ms.keywords: IQualityControl interface [DirectShow],Notify method, IQualityControl.Notify, IQualityControl::Notify, IQualityControlNotify, Notify, Notify method [DirectShow], Notify method [DirectShow],IQualityControl interface, dshow.iqualitycontrol_notify, strmif/IQualityControl::Notify
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
 - IQualityControl::Notify
 - strmif/IQualityControl::Notify
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
 - IQualityControl.Notify
---

# IQualityControl::Notify


## -description

The <code>Notify</code> method notifies the filter that a quality change is requested.

## -parameters

### -param pSelf [in]

Pointer to the filter that is sending the quality notification.

### -param q [in]

[Quality](/windows/desktop/api/strmif/ns-strmif-quality) structure.

## -returns

Returns S_OK if the method succeeds; otherwise, returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iqualitycontrol">IQualityControl Interface</a>