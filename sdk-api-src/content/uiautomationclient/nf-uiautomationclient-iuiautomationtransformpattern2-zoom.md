---
UID: NF:uiautomationclient.IUIAutomationTransformPattern2.Zoom
title: IUIAutomationTransformPattern2::Zoom
author: windows-sdk-content
description: Zooms the viewport of the control.
old-location: winauto\uiauto_IUIAutomationTransformPattern2_Zoom.htm
old-project: WinAuto
ms.assetid: 7CCDDF69-32FA-486C-B319-4D2F7A2407B4
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IUIAutomationTransformPattern2 interface [Windows Accessibility],Zoom method, IUIAutomationTransformPattern2.Zoom, IUIAutomationTransformPattern2::Zoom, Zoom, Zoom method [Windows Accessibility], Zoom method [Windows Accessibility],IUIAutomationTransformPattern2 interface, uiautomationclient/IUIAutomationTransformPattern2::Zoom, winauto.uiauto_IUIAutomationTransformPattern2_Zoom
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTransformPattern2.Zoom
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTransformPattern2::Zoom


## -description


Zooms the viewport of the control.


## -parameters




### -param zoomValue






#### - zoom [in]

Type: <b>double</b>

The amount to zoom the viewport, specified as a percentage. Positive values increase the zoom level, and negative values decrease it. The control zooms its viewport to the nearest supported value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/01585BBF-B8D7-4A69-BBB9-1B02E0864224">IUIAutomationTransformPattern2</a>
 

 

