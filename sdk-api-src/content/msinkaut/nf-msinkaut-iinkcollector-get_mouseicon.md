---
UID: NF:msinkaut.IInkCollector.get_MouseIcon
title: IInkCollector::get_MouseIcon (msinkaut.h)
description: Gets or sets the custom mouse icon. (IInkCollector.get_MouseIcon)
helpviewer_keywords: ["9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4","IInkCollector interface [Tablet PC]","MouseIcon property","IInkCollector.MouseIcon","IInkCollector.get_MouseIcon","IInkCollector::MouseIcon","IInkCollector::get_MouseIcon","IInkCollector::putref_MouseIcon","InkCollector.get_MouseIcon","MouseIcon property [Tablet PC]","MouseIcon property [Tablet PC]","IInkCollector interface","get_MouseIcon","msinkaut/IInkCollector::MouseIcon","msinkaut/IInkCollector::get_MouseIcon","msinkaut/IInkCollector::putref_MouseIcon","put_MouseIcon","tablet.inkcollector_mouseicon"]
old-location: tablet\inkcollector_mouseicon.htm
tech.root: tablet
ms.assetid: 9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4
ms.date: 12/05/2018
ms.keywords: 9c7f879a-1b6c-4bd0-8dc1-82f23ace57c4, IInkCollector interface [Tablet PC],MouseIcon property, IInkCollector.MouseIcon, IInkCollector.get_MouseIcon, IInkCollector::MouseIcon, IInkCollector::get_MouseIcon, IInkCollector::putref_MouseIcon, InkCollector.get_MouseIcon, MouseIcon property [Tablet PC], MouseIcon property [Tablet PC],IInkCollector interface, get_MouseIcon, msinkaut/IInkCollector::MouseIcon, msinkaut/IInkCollector::get_MouseIcon, msinkaut/IInkCollector::putref_MouseIcon, put_MouseIcon, tablet.inkcollector_mouseicon
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
 - IInkCollector::get_MouseIcon
 - msinkaut/IInkCollector::get_MouseIcon
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
 - IInkCollector.MouseIcon
 - IInkCollector.get_MouseIcon
 - InkCollector.get_MouseIcon
---

# IInkCollector::get_MouseIcon


## -description

Gets or sets the custom mouse icon.



This property is read/write.

## -parameters

## -remarks

The [propputref] function can accept a <b>NULL</b> reference, in which case S_OK is returned.

This property provides a custom icon that is used when the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer</a> property is set to <a href="/windows/desktop/api/msinkaut/ne-msinkaut-inkmousepointer">IMP_Custom</a>.

You can use the <b>MouseIcon</b> property to load either cursor or icon files. The <b>MouseIcon</b> property provides your application with access to custom cursors of any size with any desired hot spot location.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkcollector.md">IInkCollector</a>



<a href="/windows/desktop/tablet/inkcollector-class">InkCollector Class</a>



<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_mousepointer">MousePointer Property</a>
