---
UID: NN:d2d1.ID2D1DrawingStateBlock
title: ID2D1DrawingStateBlock (d2d1.h)
description: Represents the drawing state of a render target:\_the antialiasing mode, transform, tags, and text-rendering options.
helpviewer_keywords: ["ID2D1DrawingStateBlock","ID2D1DrawingStateBlock interface [Direct2D]","ID2D1DrawingStateBlock interface [Direct2D]","described","d2d1/ID2D1DrawingStateBlock","direct2d.ID2D1DrawingStateBlock"]
old-location: direct2d\ID2D1DrawingStateBlock.htm
tech.root: Direct2D
ms.assetid: 9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b
ms.date: 12/05/2018
ms.keywords: ID2D1DrawingStateBlock, ID2D1DrawingStateBlock interface [Direct2D], ID2D1DrawingStateBlock interface [Direct2D],described, d2d1/ID2D1DrawingStateBlock, direct2d.ID2D1DrawingStateBlock
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DrawingStateBlock
 - d2d1/ID2D1DrawingStateBlock
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DrawingStateBlock
---

# ID2D1DrawingStateBlock interface


## -description

Represents the drawing state of a render target: the antialiasing mode, transform, tags, and text-rendering options.

## -inheritance

The <b>ID2D1DrawingStateBlock</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>. <b>ID2D1DrawingStateBlock</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1DrawingStateBlock_Objects"></a><a id="creating_id2d1drawingstateblock_objects"></a><a id="CREATING_ID2D1DRAWINGSTATEBLOCK_OBJECTS"></a>Creating ID2D1DrawingStateBlock Objects</h3>
To create an <b>ID2D1DrawingStateBlock</b>, use the <a href="/windows/win32/Direct2D/id2d1factory-createdrawingstateblock">ID2D1Factory::CreateDrawingStateBlock</a> method.

A drawing state block is a device-independent resource; you can create it once and retain it for the life of your application. For more information about resources, see the <a href="/windows/win32/Direct2D/resources-and-resource-domains">Resources Overview</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1resource">ID2D1Resource</a>

