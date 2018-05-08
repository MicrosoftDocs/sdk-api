---
UID: NF:dcomp.DCompositionAttachMouseWheelToHwnd
title: DCompositionAttachMouseWheelToHwnd function
author: windows-driver-content
description: Creates an Interaction/InputSink to route mouse button down and any subsequent move and up events to the given HWND.
old-location: directcomp\dcompositionattachmousedragtohwnd.htm
old-project: directcomp
ms.assetid: 2d976c27-b7a4-5546-488a-ceb341c4fb1a
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: DCompositionAttachMouseDragToHwnd, DCompositionAttachMouseWheelToHwnd, DCompositionAttachMouseWheelToHwnd function [DirectComposition], dcomp/DCompositionAttachMouseWheelToHwnd, directcomp.dcompositionattachmousedragtohwnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: D2D_VECTOR_4F
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dcomp.dll
api_name:
-	DCompositionAttachMouseWheelToHwnd
product: Windows
targetos: Windows
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
---

# DCompositionAttachMouseWheelToHwnd function


## -description


Creates an Interaction/InputSink to route mouse button down and any 
     subsequent move and up events to the given HWND. There is no move 
     thresholding; when enabled, all events including and following the down 
     are unconditionally redirected to the specified window. After calling this 
     API, the device owning the visual must be committed.


## -parameters




### -param visual [in]

Type: <b><a href="https://msdn.microsoft.com/462dfc20-ad5a-425c-94b5-f21ab05f5af8">IDCompositionVisual</a>*</b>

The visual to route messages from.


### -param hwnd [in]

Type: <b>HWND</b>

The HWND to route messages to.


### -param enable [in]

Type: <b>BOOL</b>

Boolean value indicating whether to enable or disable routing.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



