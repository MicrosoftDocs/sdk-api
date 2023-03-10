---
UID: NF:dcomp.DCompositionAttachMouseWheelToHwnd
title: DCompositionAttachMouseWheelToHwnd function (dcomp.h)
description: Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.
helpviewer_keywords: ["DCompositionAttachMouseWheelToHwnd","DCompositionAttachMouseWheelToHwnd function [DirectComposition]","dcomp/DCompositionAttachMouseWheelToHwnd","directcomp.dcompositionattachmousewheeltohwnd"]
old-location: directcomp\dcompositionattachmousewheeltohwnd.htm
tech.root: directcomp
ms.assetid: 0a047702-e707-8df7-7660-0759a94b21af
ms.date: 12/05/2018
ms.keywords: DCompositionAttachMouseWheelToHwnd, DCompositionAttachMouseWheelToHwnd function [DirectComposition], dcomp/DCompositionAttachMouseWheelToHwnd, directcomp.dcompositionattachmousewheeltohwnd
req.header: dcomp.h
req.include-header: 
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCompositionAttachMouseWheelToHwnd
 - dcomp/DCompositionAttachMouseWheelToHwnd
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
api_name:
 - DCompositionAttachMouseWheelToHwnd
---

# DCompositionAttachMouseWheelToHwnd function


## -description

Creates an Interaction/InputSink to route mouse wheel messages to the
        given HWND.  This will fail if there is already an interaction attached
        to this visual. After calling this API, the device that owns the visual must
        be committed.

## -parameters

### -param visual [in]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>*</b>

The visual to route messages from.

### -param hwnd [in]

Type: <b>HWND</b>

The HWND to route messages to.

### -param enable [in]

Type: <b>BOOL</b>

Boolean value indicating whether to enable or disable routing.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.