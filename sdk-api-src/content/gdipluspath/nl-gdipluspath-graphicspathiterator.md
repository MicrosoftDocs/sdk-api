---
UID: NL:gdipluspath.GraphicsPathIterator
title: GraphicsPathIterator (gdipluspath.h)
description: This GraphicsPathIterator class provides methods for isolating selected subsets of the path stored in a GraphicsPath object.
helpviewer_keywords: ["GraphicsPathIterator","GraphicsPathIterator class [GDI+]","GraphicsPathIterator class [GDI+]","described","_gdiplus_CLASS_GraphicsPathIterator_Class","gdiplus._gdiplus_CLASS_GraphicsPathIterator_Class","gdipluspath/GraphicsPathIterator"]
old-location: gdiplus\_gdiplus_CLASS_GraphicsPathIterator_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\graphicspathiterator.htm
ms.date: 12/05/2018
ms.keywords: GraphicsPathIterator, GraphicsPathIterator class [GDI+], GraphicsPathIterator class [GDI+],described, _gdiplus_CLASS_GraphicsPathIterator_Class, gdiplus._gdiplus_CLASS_GraphicsPathIterator_Class, gdipluspath/GraphicsPathIterator
req.header: gdipluspath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GraphicsPathIterator
 - gdipluspath/GraphicsPathIterator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluspath.h
api_name:
 - GraphicsPathIterator
---

# GraphicsPathIterator class


## -description

This <a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspathiterator-graphicspathiterator(constgraphicspathiterator_)">GraphicsPathIterator</a> class provides methods for isolating selected subsets of the path stored in a 
			<a href="/windows/desktop/api/gdipluspath/nf-gdipluspath-graphicspath-graphicspath(constgraphicspath_)">GraphicsPath</a> object. A path consists of one or more figures. You can use a <b>GraphicsPathIterator</b> to isolate one or more of those figures. A path can also have markers that divide the path into sections. You can use a <b>GraphicsPathIterator</b> object to isolate one or more of those sections.