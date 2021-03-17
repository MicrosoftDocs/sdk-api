---
UID: NF:ctffunc.IUIManagerEventSink.OnWindowUpdated
title: IUIManagerEventSink::OnWindowUpdated (ctffunc.h)
description: Called by the TSF after resizing and/or relocating the opened IME UI.
helpviewer_keywords: ["IUIManagerEventSink interface [Text Services Framework]","OnWindowUpdated method","IUIManagerEventSink.OnWindowUpdated","IUIManagerEventSink::OnWindowUpdated","OnWindowUpdated","OnWindowUpdated method [Text Services Framework]","OnWindowUpdated method [Text Services Framework]","IUIManagerEventSink interface","ctffunc/IUIManagerEventSink::OnWindowUpdated","tsf.iuimanagereventsink_onwindowupdated"]
old-location: tsf\iuimanagereventsink_onwindowupdated.htm
tech.root: TSF
ms.assetid: A50F3F1B-B00A-4ABD-B94A-F1D3904C6938
ms.date: 12/05/2018
ms.keywords: IUIManagerEventSink interface [Text Services Framework],OnWindowUpdated method, IUIManagerEventSink.OnWindowUpdated, IUIManagerEventSink::OnWindowUpdated, OnWindowUpdated, OnWindowUpdated method [Text Services Framework], OnWindowUpdated method [Text Services Framework],IUIManagerEventSink interface, ctffunc/IUIManagerEventSink::OnWindowUpdated, tsf.iuimanagereventsink_onwindowupdated
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
 - IUIManagerEventSink::OnWindowUpdated
 - ctffunc/IUIManagerEventSink::OnWindowUpdated
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
 - IUIManagerEventSink.OnWindowUpdated
---

# IUIManagerEventSink::OnWindowUpdated


## -description

Called by the TSF after resizing and/or relocating the opened IME UI.

## -parameters

### -param prcUpdatedBounds [in]

Pointer to a <b>RECT</b> structure defining the affected area (in screen coordinates).

## -returns

Ignored.

## -see-also

<a href="/windows/desktop/api/ctffunc/nn-ctffunc-iuimanagereventsink">IUIManagerEventSink</a>