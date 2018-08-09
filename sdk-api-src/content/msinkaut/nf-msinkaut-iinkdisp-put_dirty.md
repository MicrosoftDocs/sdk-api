---
UID: NF:msinkaut.IInkDisp.put_Dirty
title: IInkDisp::put_Dirty
author: windows-sdk-content
description: Gets or sets the value that specifies whether the strokes of an InkDisp Class object have been modified since the last time the ink was saved.
old-location: tablet\inkdisp_dirty.htm
old-project: tablet
ms.assetid: 3399219f-96a5-4c66-8e41-89927ea1020d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 3399219f-96a5-4c66-8e41-89927ea1020d, Dirty property [Tablet PC], Dirty property [Tablet PC],IInkDisp interface, IInkDisp interface [Tablet PC],Dirty property, IInkDisp.Dirty, IInkDisp.put_Dirty, IInkDisp::Dirty, IInkDisp::get_Dirty, IInkDisp::put_Dirty, InkDisp.get_Dirty, InkDisp.put_Dirty, get_Dirty, msinkaut/IInkDisp::Dirty, msinkaut/IInkDisp::get_Dirty, msinkaut/IInkDisp::put_Dirty, put_Dirty, tablet.inkdisp_dirty
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
 - IInkDisp.Dirty
 - IInkDisp.get_Dirty
 - IInkDisp.put_Dirty
 - InkDisp.get_Dirty
 - InkDisp.put_Dirty
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkDisp::put_Dirty


## -description



Gets or sets the value that specifies whether the strokes of an <a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a> object have been modified since the last time the ink was saved.



This property is read/write.


## -parameters


## -remarks



After ink is saved, the dirty flag is automatically cleared and the value of this property is <b>VARIANT_FALSE</b>. To save ink, call the <a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save Method</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846797(v=VS.85).aspx">IInkDisp</a>



<a href="https://msdn.microsoft.com/f942d6a3-f303-49df-a128-de9760b508ef">InkDisp Class</a>



<a href="https://msdn.microsoft.com/31da19a7-207f-4f11-9b0f-7402e9727f59">Save Method</a>
 

 

