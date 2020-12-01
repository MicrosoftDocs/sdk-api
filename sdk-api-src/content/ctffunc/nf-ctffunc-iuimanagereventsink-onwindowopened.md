---
UID: NF:ctffunc.IUIManagerEventSink.OnWindowOpened
title: IUIManagerEventSink::OnWindowOpened (ctffunc.h)
description: Called by the TSF after opening an IME UI.
helpviewer_keywords: ["IUIManagerEventSink interface [Text Services Framework]","OnWindowOpened method","IUIManagerEventSink.OnWindowOpened","IUIManagerEventSink::OnWindowOpened","OnWindowOpened","OnWindowOpened method [Text Services Framework]","OnWindowOpened method [Text Services Framework]","IUIManagerEventSink interface","ctffunc/IUIManagerEventSink::OnWindowOpened","tsf.iuimanagereventsink_onwindowopened"]
old-location: tsf\iuimanagereventsink_onwindowopened.htm
tech.root: TSF
ms.assetid: 525500C2-313E-4430-88B1-AA1F54A420AF
ms.date: 12/05/2018
ms.keywords: IUIManagerEventSink interface [Text Services Framework],OnWindowOpened method, IUIManagerEventSink.OnWindowOpened, IUIManagerEventSink::OnWindowOpened, OnWindowOpened, OnWindowOpened method [Text Services Framework], OnWindowOpened method [Text Services Framework],IUIManagerEventSink interface, ctffunc/IUIManagerEventSink::OnWindowOpened, tsf.iuimanagereventsink_onwindowopened
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
 - IUIManagerEventSink::OnWindowOpened
 - ctffunc/IUIManagerEventSink::OnWindowOpened
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
 - IUIManagerEventSink.OnWindowOpened
---

# IUIManagerEventSink::OnWindowOpened


## -description

Called by the TSF after opening an IME UI.

## -parameters

### -param prcBounds [in]

Pointer to a <b>RECT</b> structure defining the affected area (in screen coordinates).

## -returns

Ignored.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-iuimanagereventsink">IUIManagerEventSink</a>