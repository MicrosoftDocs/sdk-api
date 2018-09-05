---
UID: NF:msinkaut.IInkPicture.get_hWnd
title: IInkPicture::get_hWnd
author: windows-sdk-content
description: Gets or sets the handle value of the window on which ink is drawn.
old-location: tablet\inkpicture_hwnd.htm
old-project: tablet
ms.assetid: c11f13f5-f0a8-45f8-83c2-372df670ef1f
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IInkPicture interface [Tablet PC],hWnd property, IInkPicture.get_hWnd, IInkPicture.hWnd, IInkPicture::get_hWnd, IInkPicture::hWnd, IInkPicture::put_hWnd, InkPicture.get_hWnd, InkPicture.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],IInkPicture interface, msinkaut/IInkPicture::get_hWnd, msinkaut/IInkPicture::hWnd, msinkaut/IInkPicture::put_hWnd, put_hWnd, tablet.inkpicture_hwnd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msinkaut.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkPicture.hWnd
 - IInkPicture.get_hWnd
 - IInkPicture.put_hWnd
 - InkPicture.get_hWnd
 - InkPicture.put_hWnd
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkPicture::get_hWnd


## -description



Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.


## -parameters


## -remarks



If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled</a> property to <b>VARIANT_FALSE</b>. You can then set the <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd</a> property and re-enable the object by setting the <b>Enabled</b> property to <b>VARIANT_TRUE</b>.</div>
<div> </div>
In Automation, this property is called <a href="https://msdn.microsoft.com/1a8b933f-a4f0-46f5-8b41-df89b6378e9f">hWnd Property</a>.




## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="https://msdn.microsoft.com/EA6AC3DD-5F13-442A-B93D-FF0A5333609A">IInkPicture</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>
 

 

