---
UID: NF:ctffunc.IUIManagerEventSink.OnWindowOpening
title: IUIManagerEventSink::OnWindowOpening (ctffunc.h)
description: Called by the TSF before opening an IME UI.
helpviewer_keywords: ["IUIManagerEventSink interface [Text Services Framework]","OnWindowOpening method","IUIManagerEventSink.OnWindowOpening","IUIManagerEventSink::OnWindowOpening","OnWindowOpening","OnWindowOpening method [Text Services Framework]","OnWindowOpening method [Text Services Framework]","IUIManagerEventSink interface","ctffunc/IUIManagerEventSink::OnWindowOpening","tsf.iuimanagereventsink_onwindowopening"]
old-location: tsf\iuimanagereventsink_onwindowopening.htm
tech.root: TSF
ms.assetid: B384AC51-2544-429B-ADEC-1D45CCB178FB
ms.date: 12/05/2018
ms.keywords: IUIManagerEventSink interface [Text Services Framework],OnWindowOpening method, IUIManagerEventSink.OnWindowOpening, IUIManagerEventSink::OnWindowOpening, OnWindowOpening, OnWindowOpening method [Text Services Framework], OnWindowOpening method [Text Services Framework],IUIManagerEventSink interface, ctffunc/IUIManagerEventSink::OnWindowOpening, tsf.iuimanagereventsink_onwindowopening
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
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
 - IUIManagerEventSink::OnWindowOpening
 - ctffunc/IUIManagerEventSink::OnWindowOpening
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ctffunc.h
api_name:
 - IUIManagerEventSink.OnWindowOpening
---

# IUIManagerEventSink::OnWindowOpening


## -description

Called by the TSF before opening an IME UI.

## -parameters

### -param prcBounds [in]

Pointer to a <b>RECT</b> structure defining the affected area (in screen coordinates).

## -returns

Ignored.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-iuimanagereventsink">IUIManagerEventSink</a>