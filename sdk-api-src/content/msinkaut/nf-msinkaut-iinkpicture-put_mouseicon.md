---
UID: NF:msinkaut.IInkPicture.put_MouseIcon
title: IInkPicture::put_MouseIcon (msinkaut.h)
author: windows-sdk-content
description: Gets or sets the custom mouse icon.
old-location: tablet\inkpicture_mouseicon.htm
tech.root: tablet
ms.assetid: a095dca7-4dc9-4661-8c78-0e357a57f982
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInkPicture interface [Tablet PC],MouseIcon property, IInkPicture.MouseIcon, IInkPicture.put_MouseIcon, IInkPicture::MouseIcon, IInkPicture::get_MouseIcon, IInkPicture::put_MouseIcon, InkPicture.get_MouseIcon, InkPicture.put_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkPicture interface, get_MouseIcon, msinkaut/IInkPicture::MouseIcon, msinkaut/IInkPicture::get_MouseIcon, msinkaut/IInkPicture::put_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkpicture_mouseicon
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
 - IInkPicture.MouseIcon
 - IInkPicture.get_MouseIcon
 - IInkPicture.put_MouseIcon
 - InkPicture.get_MouseIcon
 - InkPicture.put_MouseIcon
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkPicture::put_MouseIcon


## -description



Gets or sets the custom mouse icon.



This property is read/write.


## -parameters


## -remarks



The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="https://msdn.microsoft.com/94536770-01ef-41c5-9217-0aa2ef9c36ac">MousePointer</a> property is set to <a href="https://msdn.microsoft.com/74f489f2-d568-4133-96e6-de15cbfabfe7">IMP_Custom</a>.

You can use the <b>MouseIcon</b> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://msdn.microsoft.com/189f430e-9d00-4e29-bb8c-8ac195896793">InkCollector</a>



<a href="https://msdn.microsoft.com/1ced9779-dae5-4f9a-8a68-b2c0d041d5b4">InkPicture Control</a>



<a href="https://msdn.microsoft.com/94536770-01ef-41c5-9217-0aa2ef9c36ac">MousePointer Property</a>
 

 

