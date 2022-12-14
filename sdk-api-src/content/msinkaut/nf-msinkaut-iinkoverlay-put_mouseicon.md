---
UID: NF:msinkaut.IInkOverlay.put_MouseIcon
title: IInkOverlay::put_MouseIcon (msinkaut.h)
description: Gets or sets the custom mouse icon. (IInkOverlay.put_MouseIcon)
helpviewer_keywords: ["IInkOverlay interface [Tablet PC]","MouseIcon property","IInkOverlay.MouseIcon","IInkOverlay.put_MouseIcon","IInkOverlay::MouseIcon","IInkOverlay::get_MouseIcon","IInkOverlay::put_MouseIcon","InkOverlay.get_MouseIcon","InkOverlay.put_MouseIcon","MouseIcon property [Tablet PC]","MouseIcon property [Tablet PC]","IInkOverlay interface","get_MouseIcon","msinkaut/IInkOverlay::MouseIcon","msinkaut/IInkOverlay::get_MouseIcon","msinkaut/IInkOverlay::put_MouseIcon","put_MouseIcon","putref_MouseIcon","tablet.inkoverlay_mouseicon"]
old-location: tablet\inkoverlay_mouseicon.htm
tech.root: tablet
ms.assetid: 4bfc82db-9086-4ad5-9db0-84d7fedadec0
ms.date: 12/05/2018
ms.keywords: IInkOverlay interface [Tablet PC],MouseIcon property, IInkOverlay.MouseIcon, IInkOverlay.put_MouseIcon, IInkOverlay::MouseIcon, IInkOverlay::get_MouseIcon, IInkOverlay::put_MouseIcon, InkOverlay.get_MouseIcon, InkOverlay.put_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkOverlay interface, get_MouseIcon, msinkaut/IInkOverlay::MouseIcon, msinkaut/IInkOverlay::get_MouseIcon, msinkaut/IInkOverlay::put_MouseIcon, put_MouseIcon, putref_MouseIcon, tablet.inkoverlay_mouseicon
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkOverlay::put_MouseIcon
 - msinkaut/IInkOverlay::put_MouseIcon
dev_langs:
 - c++
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
---

# IInkOverlay::put_MouseIcon


## -description

Gets or sets the custom mouse icon.



This property is read/write.

## -parameters

## -remarks

The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer</a> property is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Custom</a>.

You can use the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mouseicon">MouseIcon</a> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkoverlay.md">IInkOverlay</a>



<a href="/windows/desktop/tablet/inkoverlay-class">InkOverlay Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer Property</a>
