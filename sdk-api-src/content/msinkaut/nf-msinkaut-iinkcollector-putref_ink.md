---
UID: NF:msinkaut.IInkCollector.putref_Ink
title: IInkCollector::putref_Ink
author: windows-sdk-content
description: Gets or sets the InkDisp object that is associated with an InkCollector object or an InkOverlay object.
old-location: tablet\inkcollector_ink.htm
old-project: tablet
ms.assetid: 62881a0e-3932-49a1-8e7d-3e74474f2214
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: 62881a0e-3932-49a1-8e7d-3e74474f2214, IInkCollector interface [Tablet PC],Ink property, IInkCollector.Ink, IInkCollector.get_Ink, IInkCollector.putref_Ink, IInkCollector::Ink, IInkCollector::get_Ink, IInkCollector::putref_Ink, Ink property [Tablet PC], Ink property [Tablet PC],IInkCollector interface, InkCollector.get_Ink, get_Ink, msinkaut/IInkCollector::Ink, msinkaut/IInkCollector::get_Ink, msinkaut/IInkCollector::putref_Ink, putref_Ink, tablet.inkcollector_ink
ms.prod: windows
ms.technology: windows-sdk
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
 - IInkCollector.Ink
 - IInkCollector.get_Ink
 - get_Ink
 - IInkCollector.get_Ink
 - InkCollector.get_Ink
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::putref_Ink


## -description



Gets or sets the <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object that is associated with an <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or an <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object.



This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> object or the <a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay</a> object must be disabled before setting this property. To disable the <b>InkCollector</b> object or the <b>InkOverlay</b> object, set the <a href="https://msdn.microsoft.com/library/windows/hardware/dn966102">Enabled</a> property to <b>FALSE</b>. You can then set the <b>Ink</b> property, and re-enable the object by setting the <b>Enabled</b> property to <b>TRUE</b>.</div>
<div> </div>
An <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> creates an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp</a> object by default. If two or more <b>InkDisp</b> objects exist on a known application window, they can be switched out to enable collection into any of them (such as after deserializing one of the <b>InkDisp</b> objects).




## -see-also




<a href="https://msdn.microsoft.com/ab55a399-1990-4cfc-a4ab-834a5db8d7a9">Enabled Property</a>



<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>
 

 

