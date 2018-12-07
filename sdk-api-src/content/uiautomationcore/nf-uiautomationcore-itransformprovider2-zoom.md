---
UID: NF:uiautomationcore.ITransformProvider2.Zoom
title: ITransformProvider2::Zoom
author: windows-sdk-content
description: Zooms the viewport of the control.
old-location: winauto\uiauto_ITransformProvider2_Zoom.htm
tech.root: WinAuto
ms.assetid: B267DAB1-F78B-4543-9A90-7107E5259A0C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITransformProvider2 interface [Windows Accessibility],Zoom method, ITransformProvider2.Zoom, ITransformProvider2::Zoom, Zoom, Zoom method [Windows Accessibility], Zoom method [Windows Accessibility],ITransformProvider2 interface, uiautomationcore/ITransformProvider2::Zoom, winauto.uiauto_ITransformProvider2_Zoom
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITransformProvider2.Zoom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITransformProvider2::Zoom


## -description


Zooms the viewport of the control. 


## -parameters




### -param zoom [in]

Type: <b>double</b>

The amount to zoom the viewport, specified as a percentage. The provider should zoom the viewport to the nearest supported value.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/763F30BC-782A-43ED-9DE4-97A237D7B9F8">ITransformProvider2</a>
 

 

