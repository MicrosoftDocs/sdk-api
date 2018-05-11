---
UID: NF:msinkaut.IInkCollector.put_hWnd
title: IInkCollector::put_hWnd
author: windows-driver-content
description: Gets or sets the handle value of the window on which ink is drawn.
old-location: tablet\inkcollector_hwnd.htm
old-project: tablet
ms.assetid: 1a8b933f-a4f0-46f5-8b41-df89b6378e9f
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: 1a8b933f-a4f0-46f5-8b41-df89b6378e9f, IInkCollector.put_hWnd, IInkCollector::put_hWnd, InkCollector class [Tablet PC],hWnd property, InkCollector.get_hWnd, InkCollector.hWnd, InkCollector.put_hWnd, get_hWnd, hWnd property [Tablet PC], hWnd property [Tablet PC],InkCollector class, put_hWnd, tablet.inkcollector_hwnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msinkaut.h
req.include-header: 
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
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	InkCollector.hWnd
-	put_hWnd
-	IInkCollector.put_hWnd
-	InkCollector.get_hWnd
-	InkCollector.put_hWnd
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IInkCollector::put_hWnd


## -description



Gets or sets the handle value of the window on which ink is drawn.



This property is read/write.


## -parameters


## -remarks



If two or more windows exist, this property allows you to specify which window collects ink.

<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> or <b>InkOverlay</b> objects, set the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property to <b>FALSE</b>. You can then set the <b>hWnd</b> property and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
In Automation, this property is called <b>hWnd Property</b>.




## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

