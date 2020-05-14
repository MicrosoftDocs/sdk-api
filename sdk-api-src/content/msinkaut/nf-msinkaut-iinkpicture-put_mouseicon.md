---
UID: NF:msinkaut.IInkPicture.put_MouseIcon
title: IInkPicture::put_MouseIcon (msinkaut.h)
description: Gets or sets the custom mouse icon.helpviewer_keywords: ["IInkPicture interface [Tablet PC]","MouseIcon property","IInkPicture.MouseIcon","IInkPicture.put_MouseIcon","IInkPicture::MouseIcon","IInkPicture::get_MouseIcon","IInkPicture::put_MouseIcon","InkPicture.get_MouseIcon","InkPicture.put_MouseIcon","MouseIcon property [Tablet PC]","MouseIcon property [Tablet PC]","IInkPicture interface","get_MouseIcon","msinkaut/IInkPicture::MouseIcon","msinkaut/IInkPicture::get_MouseIcon","msinkaut/IInkPicture::put_MouseIcon","put_MouseIcon","putref_MouseIcon","tablet.inkpicture_mouseicon"]
old-location: tablet\inkpicture_mouseicon.htm
tech.root: tablet
ms.assetid: a095dca7-4dc9-4661-8c78-0e357a57f982
ms.date: 12/05/2018
ms.keywords: IInkPicture interface [Tablet PC],MouseIcon property, IInkPicture.MouseIcon, IInkPicture.put_MouseIcon, IInkPicture::MouseIcon, IInkPicture::get_MouseIcon, IInkPicture::put_MouseIcon, InkPicture.get_MouseIcon, InkPicture.put_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkPicture interface, get_MouseIcon, msinkaut/IInkPicture::MouseIcon, msinkaut/IInkPicture::get_MouseIcon, msinkaut/IInkPicture::put_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkpicture_mouseicon
f1_keywords:
- msinkaut/IInkPicture.MouseIcon
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInkPicture::put_MouseIcon


## -description



Gets or sets the custom mouse icon.



This property is read/write.


## -parameters


## -remarks



The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer">MousePointer</a> property is set to <a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Custom</a>.

You can use the <b>MouseIcon</b> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt846800(v=VS.85).aspx">IInkPicture</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkcollector-class">InkCollector</a>



<a href="https://docs.microsoft.com/windows/desktop/tablet/inkpicture-control">InkPicture Control</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_mousepointer">MousePointer Property</a>
 

 

