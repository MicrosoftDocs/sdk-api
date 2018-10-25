---
UID: NF:dcomp.DCompositionAttachMouseWheelToHwnd
title: DCompositionAttachMouseWheelToHwnd function
author: windows-sdk-content
description: Creates an Interaction/InputSink to route mouse wheel messages to the given HWND.
old-location: directcomp\dcompositionattachmousewheeltohwnd.htm
tech.root: directcomp
ms.assetid: 0a047702-e707-8df7-7660-0759a94b21af
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DCompositionAttachMouseWheelToHwnd, DCompositionAttachMouseWheelToHwnd function [DirectComposition], dcomp/DCompositionAttachMouseWheelToHwnd, directcomp.dcompositionattachmousewheeltohwnd
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
api_name:
 - DCompositionAttachMouseWheelToHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DCompositionAttachMouseWheelToHwnd function


## -description


Creates an Interaction/InputSink to route mouse wheel messages to the
        given HWND.  This will fail if there is already an interaction attached
        to this visual. After calling this API, the device that owns the visual must
        be committed.
      


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



