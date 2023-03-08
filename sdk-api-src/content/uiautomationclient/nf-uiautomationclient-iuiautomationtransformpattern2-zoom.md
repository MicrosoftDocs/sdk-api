---
UID: NF:uiautomationclient.IUIAutomationTransformPattern2.Zoom
title: IUIAutomationTransformPattern2::Zoom (uiautomationclient.h)
description: Zooms the viewport of the control. (IUIAutomationTransformPattern2.Zoom)
helpviewer_keywords: ["IUIAutomationTransformPattern2 interface [Windows Accessibility]","Zoom method","IUIAutomationTransformPattern2.Zoom","IUIAutomationTransformPattern2::Zoom","Zoom","Zoom method [Windows Accessibility]","Zoom method [Windows Accessibility]","IUIAutomationTransformPattern2 interface","uiautomationclient/IUIAutomationTransformPattern2::Zoom","winauto.uiauto_IUIAutomationTransformPattern2_Zoom"]
old-location: winauto\uiauto_IUIAutomationTransformPattern2_Zoom.htm
tech.root: WinAuto
ms.assetid: 7CCDDF69-32FA-486C-B319-4D2F7A2407B4
ms.date: 12/05/2018
ms.keywords: IUIAutomationTransformPattern2 interface [Windows Accessibility],Zoom method, IUIAutomationTransformPattern2.Zoom, IUIAutomationTransformPattern2::Zoom, Zoom, Zoom method [Windows Accessibility], Zoom method [Windows Accessibility],IUIAutomationTransformPattern2 interface, uiautomationclient/IUIAutomationTransformPattern2::Zoom, winauto.uiauto_IUIAutomationTransformPattern2_Zoom
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationTransformPattern2::Zoom
 - uiautomationclient/IUIAutomationTransformPattern2::Zoom
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTransformPattern2.Zoom
---

# IUIAutomationTransformPattern2::Zoom


## -description

Zooms the viewport of the control.

## -parameters

### -param zoomValue [in]

Type: <b>double</b>

The amount to zoom the viewport, specified as a percentage. Positive values increase the zoom level, and negative values decrease it. The control zooms its viewport to the nearest supported value.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtransformpattern2">IUIAutomationTransformPattern2</a>
