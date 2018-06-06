---
UID: NF:msinkaut.IInkCollector.putref_Renderer
title: IInkCollector::putref_Renderer
author: windows-sdk-content
description: Gets or sets the InkRenderer object that is used to draw ink.
old-location: tablet\inkcollector_renderer.htm
old-project: tablet
ms.assetid: 1abd8f85-88f5-4dc6-a0b8-9156b57c57a5
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: 1abd8f85-88f5-4dc6-a0b8-9156b57c57a5, IInkCollector interface [Tablet PC],Renderer property, IInkCollector.Renderer, IInkCollector.putref_Renderer, IInkCollector::Renderer, IInkCollector::get_Renderer, IInkCollector::putref_Renderer, InkCollector.get_Renderer, Put_Renderer, Renderer property [Tablet PC], Renderer property [Tablet PC],IInkCollector interface, get_Renderer, msinkaut/IInkCollector::Renderer, msinkaut/IInkCollector::get_Renderer, msinkaut/IInkCollector::putref_Renderer, putref_Renderer, tablet.inkcollector_renderer
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
 - IInkCollector.Renderer
 - IInkCollector.get_Renderer
 - InkCollector.get_Renderer
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkCollector::putref_Renderer


## -description



Gets or sets the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">InkRenderer</a> object that is used to draw ink.



This property is read/write.


## -parameters


## -remarks



When handling certain window messages, changing the <a href="https://msdn.microsoft.com/66ec7cab-bfc2-4934-93a4-0ab9cb8c96e7">Renderer</a> associated with the <a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a> can cause a reentrant function call, generating unexpected results. For example, changing to a different <i>Renderer</i> or modifying its transforms within a message handler can result in a reentrant call. This affects the following messages: <b>WM_ACTIVATE</b>, <b>WM_ACTIVATEAPP</b>, <b>WM_NCACTIVATE</b>, <b>WM_PAINT</b>; <b>WM_SYSCOMMAND</b> if <i>wParam</i> is set to SC_HOTKEY or SC_TASKLIST; and <b>WM_SYSKEYDOWN</b> (when processing Alt-Tab or Alt-Esc key combinations). It is an issue with single-threaded apartment model applications.




## -see-also




<a href="tablet.iinkcollector">IInkCollector</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector Class</a>
 

 

