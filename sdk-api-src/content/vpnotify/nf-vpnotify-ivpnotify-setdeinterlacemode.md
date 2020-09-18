---
UID: NF:vpnotify.IVPNotify.SetDeinterlaceMode
title: IVPNotify::SetDeinterlaceMode (vpnotify.h)
description: Sets the mode (such as bob or weave).
helpviewer_keywords: ["IVPNotify interface [DirectShow]","SetDeinterlaceMode method","IVPNotify.SetDeinterlaceMode","IVPNotify::SetDeinterlaceMode","IVPNotifySetDeinterlaceMode","SetDeinterlaceMode","SetDeinterlaceMode method [DirectShow]","SetDeinterlaceMode method [DirectShow]","IVPNotify interface","dshow.ivpnotify_setdeinterlacemode","vpnotify/IVPNotify::SetDeinterlaceMode"]
old-location: dshow\ivpnotify_setdeinterlacemode.htm
tech.root: dshow
ms.assetid: 41984fb1-7276-4232-b19a-d251c9fcd699
ms.date: 12/05/2018
ms.keywords: IVPNotify interface [DirectShow],SetDeinterlaceMode method, IVPNotify.SetDeinterlaceMode, IVPNotify::SetDeinterlaceMode, IVPNotifySetDeinterlaceMode, SetDeinterlaceMode, SetDeinterlaceMode method [DirectShow], SetDeinterlaceMode method [DirectShow],IVPNotify interface, dshow.ivpnotify_setdeinterlacemode, vpnotify/IVPNotify::SetDeinterlaceMode
req.header: vpnotify.h
req.include-header: 
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
 - IVPNotify::SetDeinterlaceMode
 - vpnotify/IVPNotify::SetDeinterlaceMode
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
 - IVPNotify.SetDeinterlaceMode
---

# IVPNotify::SetDeinterlaceMode


## -description

Sets the mode (such as bob or weave).

## -parameters

### -param mode [in]

Specified mode. This value is a member of the <a href="/previous-versions/windows/desktop/api/vptype/ne-vptype-amvp_mode">AMVP_MODE</a> enumerated data type.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify Interface</a>