---
UID: NN:msinkaut.IInkRenderer
title: IInkRenderer (msinkaut.h)
description: . (IInkRenderer)
helpviewer_keywords: ["IInkRenderer","IInkRenderer interface [Tablet PC]","IInkRenderer interface [Tablet PC]","described","msinkaut/IInkRenderer","tablet.iinkrenderer"]
old-location: tablet\iinkrenderer.htm
tech.root: tablet
ms.assetid: 2AB56616-3F67-4428-8A99-FCE733A5FDBF
ms.date: 12/05/2018
ms.keywords: IInkRenderer, IInkRenderer interface [Tablet PC], IInkRenderer interface [Tablet PC],described, msinkaut/IInkRenderer, tablet.iinkrenderer
req.header: msinkaut.h
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
 - IInkRenderer
 - msinkaut/IInkRenderer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msinkaut.h
api_name:
 - IInkRenderer
---

# IInkRenderer interface


## -description

Represents the management of mappings from ink to the display window. Use the InkRenderer object to display ink in a window. You can also use it to reposition and resize stroke.

## -inheritance

The <b>IInkRenderer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInkRenderer</b> also has these types of members:

## -remarks

Printing is also done through the InkRenderer object.

This object can be instantiated by calling the [CoCreateInstance](../combaseapi/nf-combaseapi-cocreateinstance.md) method in C++.

## -see-also

[InkRenderer class](/windows/win32/tablet/inkrenderer-class)
