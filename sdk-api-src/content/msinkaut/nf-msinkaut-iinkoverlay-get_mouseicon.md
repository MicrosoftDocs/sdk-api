---
UID: NF:msinkaut.IInkOverlay.get_MouseIcon
title: IInkOverlay::get_MouseIcon
author: windows-sdk-content
description: Gets or sets the custom mouse icon.
old-location: tablet\inkoverlay_mouseicon.htm
tech.root: tablet
ms.assetid: 4bfc82db-9086-4ad5-9db0-84d7fedadec0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkOverlay interface [Tablet PC],MouseIcon property, IInkOverlay.MouseIcon, IInkOverlay.get_MouseIcon, IInkOverlay::MouseIcon, IInkOverlay::get_MouseIcon, IInkOverlay::put_MouseIcon, InkOverlay.get_MouseIcon, InkOverlay.put_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkOverlay interface, get_MouseIcon, msinkaut/IInkOverlay::MouseIcon, msinkaut/IInkOverlay::get_MouseIcon, msinkaut/IInkOverlay::put_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkoverlay_mouseicon
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkOverlay.MouseIcon
 - IInkOverlay.get_MouseIcon
 - IInkOverlay.put_MouseIcon
 - InkOverlay.get_MouseIcon
 - InkOverlay.put_MouseIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkOverlay::get_MouseIcon


## -description



Gets or sets the custom mouse icon.



This property is read/write.


## -parameters


## -remarks



The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer</a> property is set to <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Custom</a>.

You can use the <a href="https://msdn.microsoft.com/9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4">MouseIcon</a> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846799(v=VS.85).aspx">IInkOverlay</a>



<a href="https://msdn.microsoft.com/61191ab3-075e-458b-9e0f-4bc255687b3c">InkOverlay Class</a>



<a href="https://msdn.microsoft.com/8876b0ef-1a61-481b-ac37-9e4d637f8097">MousePointer Property</a>
 

 

