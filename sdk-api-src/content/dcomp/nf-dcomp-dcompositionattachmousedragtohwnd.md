---
UID: NF:dcomp.DCompositionAttachMouseDragToHwnd
title: DCompositionAttachMouseDragToHwnd function (dcomp.h)
description: Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.
helpviewer_keywords: ["DCompositionAttachMouseDragToHwnd","DCompositionAttachMouseDragToHwnd function [DirectComposition]","dcomp/DCompositionAttachMouseDragToHwnd","directcomp.dcompositionattachmousedragtohwnd"]
old-location: directcomp\dcompositionattachmousedragtohwnd.htm
tech.root: directcomp
ms.assetid: 2d976c27-b7a4-5546-488a-ceb341c4fb1a
ms.date: 12/05/2018
ms.keywords: DCompositionAttachMouseDragToHwnd, DCompositionAttachMouseDragToHwnd function [DirectComposition], dcomp/DCompositionAttachMouseDragToHwnd, directcomp.dcompositionattachmousedragtohwnd
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
 - DCompositionAttachMouseDragToHwnd
 - dcomp/DCompositionAttachMouseDragToHwnd
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
 - DCompositionAttachMouseDragToHwnd
---

# DCompositionAttachMouseDragToHwnd function


## -description

Creates an Interaction/InputSink to route mouse button down and any 
     subsequent move and up events to the given HWND. There is no move 
     thresholding; when enabled, all events including and following the down 
     are unconditionally redirected to the specified window. After calling this 
     API, the device owning the visual must be committed.

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