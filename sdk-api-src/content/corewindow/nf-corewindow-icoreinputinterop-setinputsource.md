---
UID: NF:corewindow.ICoreInputInterop.SetInputSource
title: ICoreInputInterop::SetInputSource (corewindow.h)
description: Sets the input source for an app's CoreIndependentInputSource or CoreComponentInputSource.
helpviewer_keywords: ["ICoreInputInterop interface [Windows Runtime]","SetInputSource method","ICoreInputInterop.SetInputSource","ICoreInputInterop::SetInputSource","SetInputSource","SetInputSource method [Windows Runtime]","SetInputSource method [Windows Runtime]","ICoreInputInterop interface","corewindow/ICoreInputInterop::SetInputSource","winrt.icoreinputinterop_setinputsource"]
old-location: winrt\icoreinputinterop_setinputsource.htm
tech.root: WinRT
ms.assetid: 693180F5-2C19-47CD-9514-F0CEA1849A4A
ms.date: 08/03/2022
ms.keywords: ICoreInputInterop interface [Windows Runtime],SetInputSource method, ICoreInputInterop.SetInputSource, ICoreInputInterop::SetInputSource, SetInputSource, SetInputSource method [Windows Runtime], SetInputSource method [Windows Runtime],ICoreInputInterop interface, corewindow/ICoreInputInterop::SetInputSource, winrt.icoreinputinterop_setinputsource
req.header: corewindow.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICoreInputInterop::SetInputSource
 - corewindow/ICoreInputInterop::SetInputSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - corewindow.h
api_name:
 - ICoreInputInterop.SetInputSource
---

# ICoreInputInterop::SetInputSource


## -description

Sets the input source for an app's <a href="/uwp/api/windows.ui.core.coreindependentinputsource">CoreIndependentInputSource</a> or <a href="/uwp/api/windows.ui.core.corecomponentinputsource">CoreComponentInputSource</a>.

## -parameters

### -param value [in]

Pointer to the base COM interface of the input source.

The input source can be either <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual2">IDCompositionVisual2</a> or <a href="/uwp/api/windows.ui.composition.visual">Windows.UI.Composition.Visual</a>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/uwp/api/windows.ui.core.corecomponentinputsource">CoreComponentInputSource</a>



<a href="/uwp/api/windows.ui.core.coreindependentinputsource">CoreIndependentInputSource</a>



<a href="/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop">ICoreInputInterop</a>