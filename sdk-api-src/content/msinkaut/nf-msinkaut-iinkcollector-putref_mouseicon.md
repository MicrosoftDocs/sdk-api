---
UID: NF:msinkaut.IInkCollector.putref_MouseIcon
title: IInkCollector::putref_MouseIcon
author: windows-sdk-content
description: Gets or sets the custom mouse icon.
old-location: tablet\inkcollector_mouseicon.htm
old-project: tablet
ms.assetid: 9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4, IInkCollector interface [Tablet PC],MouseIcon property, IInkCollector.MouseIcon, IInkCollector.putref_MouseIcon, IInkCollector::MouseIcon, IInkCollector::get_MouseIcon, IInkCollector::putref_MouseIcon, InkCollector.get_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkCollector interface, get_MouseIcon, msinkaut/IInkCollector::MouseIcon, msinkaut/IInkCollector::get_MouseIcon, msinkaut/IInkCollector::putref_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkcollector_mouseicon
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
 - IInkCollector.MouseIcon
 - IInkCollector.get_MouseIcon
 - InkCollector.get_MouseIcon
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::putref_MouseIcon


## -description



Gets or sets the custom mouse icon.



This property is read/write.


## -parameters


## -remarks



The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer</a> property is set to <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Custom</a>.

You can use the <b>MouseIcon</b> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.




## -see-also




<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>



<a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer Property</a>
 

 

