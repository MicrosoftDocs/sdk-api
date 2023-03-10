---
UID: NF:msinkaut.IInkDrawingAttributes.get_AntiAliased
title: IInkDrawingAttributes::get_AntiAliased (msinkaut.h)
description: Gets or sets the value that indicates whether a stroke is antialiased. (Get)
helpviewer_keywords: ["3536cd42-372d-4bd7-ac69-ef8d6c07f7fd","AntiAliased property [Tablet PC]","AntiAliased property [Tablet PC]","IInkDrawingAttributes interface","IInkDrawingAttributes interface [Tablet PC]","AntiAliased property","IInkDrawingAttributes.AntiAliased","IInkDrawingAttributes.get_AntiAliased","IInkDrawingAttributes::AntiAliased","IInkDrawingAttributes::get_AntiAliased","IInkDrawingAttributes::put_AntiAliased","InkDrawingAttributes.get_AntiAliased","InkDrawingAttributes.put_AntiAliased","get_AntiAliased","msinkaut/IInkDrawingAttributes::AntiAliased","msinkaut/IInkDrawingAttributes::get_AntiAliased","msinkaut/IInkDrawingAttributes::put_AntiAliased","put_AntiAliased","tablet.inkdrawingattributes_antialiased"]
old-location: tablet\inkdrawingattributes_antialiased.htm
tech.root: tablet
ms.assetid: 3536cd42-372d-4bd7-ac69-ef8d6c07f7fd
ms.date: 12/05/2018
ms.keywords: 3536cd42-372d-4bd7-ac69-ef8d6c07f7fd, AntiAliased property [Tablet PC], AntiAliased property [Tablet PC],IInkDrawingAttributes interface, IInkDrawingAttributes interface [Tablet PC],AntiAliased property, IInkDrawingAttributes.AntiAliased, IInkDrawingAttributes.get_AntiAliased, IInkDrawingAttributes::AntiAliased, IInkDrawingAttributes::get_AntiAliased, IInkDrawingAttributes::put_AntiAliased, InkDrawingAttributes.get_AntiAliased, InkDrawingAttributes.put_AntiAliased, get_AntiAliased, msinkaut/IInkDrawingAttributes::AntiAliased, msinkaut/IInkDrawingAttributes::get_AntiAliased, msinkaut/IInkDrawingAttributes::put_AntiAliased, put_AntiAliased, tablet.inkdrawingattributes_antialiased
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
 - IInkDrawingAttributes::get_AntiAliased
 - msinkaut/IInkDrawingAttributes::get_AntiAliased
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
 - IInkDrawingAttributes.AntiAliased
 - IInkDrawingAttributes.get_AntiAliased
 - IInkDrawingAttributes.put_AntiAliased
 - InkDrawingAttributes.get_AntiAliased
 - InkDrawingAttributes.put_AntiAliased
---

# IInkDrawingAttributes::get_AntiAliased


## -description

Gets or sets the value that indicates whether a stroke is antialiased.



This property is read/write.

## -parameters

## -remarks

If a stroke is antialiased, the foreground and background colors along the edge of the ink are blended to increase the visible smoothness.

Antialiasing improves the quality of rendering by making ink appear smoother and sharper, especially on lower resolution displays. However, antialiasing incurs added performance. Use it judiciously.

## -see-also

<a href="../msinkaut/nn-msinkaut-iinkdrawingattributes.md">IInkDrawingAttributes</a>



<a href="/windows/desktop/tablet/inkdrawingattributes-class">InkDrawingAttribute Class</a>
