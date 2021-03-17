---
UID: NF:vpnotify.IVPNotify.GetDeinterlaceMode
title: IVPNotify::GetDeinterlaceMode (vpnotify.h)
description: The GetDeinterlaceMode method retrieves the mode (such as bob or weave).
helpviewer_keywords: ["GetDeinterlaceMode","GetDeinterlaceMode method [DirectShow]","GetDeinterlaceMode method [DirectShow]","IVPNotify interface","IVPNotify interface [DirectShow]","GetDeinterlaceMode method","IVPNotify.GetDeinterlaceMode","IVPNotify::GetDeinterlaceMode","IVPNotifyGetDeinterlaceMode","dshow.ivpnotify_getdeinterlacemode","vpnotify/IVPNotify::GetDeinterlaceMode"]
old-location: dshow\ivpnotify_getdeinterlacemode.htm
tech.root: dshow
ms.assetid: 08d28857-5460-407d-a169-8568b2c381e6
ms.date: 12/05/2018
ms.keywords: GetDeinterlaceMode, GetDeinterlaceMode method [DirectShow], GetDeinterlaceMode method [DirectShow],IVPNotify interface, IVPNotify interface [DirectShow],GetDeinterlaceMode method, IVPNotify.GetDeinterlaceMode, IVPNotify::GetDeinterlaceMode, IVPNotifyGetDeinterlaceMode, dshow.ivpnotify_getdeinterlacemode, vpnotify/IVPNotify::GetDeinterlaceMode
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
 - IVPNotify::GetDeinterlaceMode
 - vpnotify/IVPNotify::GetDeinterlaceMode
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
 - IVPNotify.GetDeinterlaceMode
---

# IVPNotify::GetDeinterlaceMode


## -description

The <code>GetDeinterlaceMode</code> method retrieves the mode (such as bob or weave).



This method is not currently implemented and returns E_NOTIMPL.

## -parameters

### -param pMode [out]

Pointer to the retrieved mode. This value is a member of the <a href="/previous-versions/windows/desktop/api/vptype/ne-vptype-amvp_mode">AMVP_MODE</a> enumerated data type.

## -returns

Returns E_NOTIMPL.

## -remarks

Include Vptype.h before Vpnotify.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpnotify/nn-vpnotify-ivpnotify">IVPNotify Interface</a>