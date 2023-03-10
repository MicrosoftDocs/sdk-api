---
UID: NN:d2d1.ID2D1SimplifiedGeometrySink
title: ID2D1SimplifiedGeometrySink (d2d1.h)
description: Describes a geometric path that does not contain quadratic bezier curves or arcs.
helpviewer_keywords: ["ID2D1SimplifiedGeometrySink","ID2D1SimplifiedGeometrySink interface [Direct2D]","ID2D1SimplifiedGeometrySink interface [Direct2D]","described","d2d1/ID2D1SimplifiedGeometrySink","direct2d.ID2D1SimplifiedGeometrySink"]
old-location: direct2d\ID2D1SimplifiedGeometrySink.htm
tech.root: Direct2D
ms.assetid: cf877a25-7b9f-4db0-ac53-b4a350795a86
ms.date: 12/05/2018
ms.keywords: ID2D1SimplifiedGeometrySink, ID2D1SimplifiedGeometrySink interface [Direct2D], ID2D1SimplifiedGeometrySink interface [Direct2D],described, d2d1/ID2D1SimplifiedGeometrySink, direct2d.ID2D1SimplifiedGeometrySink
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
 - ID2D1SimplifiedGeometrySink
 - d2d1/ID2D1SimplifiedGeometrySink
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
 - ID2D1SimplifiedGeometrySink
---

# ID2D1SimplifiedGeometrySink interface


## -description

Describes a geometric path that does not contain quadratic bezier curves or arcs.

## -inheritance

The <b>ID2D1SimplifiedGeometrySink</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID2D1SimplifiedGeometrySink</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

A geometry sink consists of one or more figures. Each figure is made up of one or more line or Bezier curve segments. To create a figure, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure">BeginFigure</a> method and specify the figure's start point, then use <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines">AddLines</a> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addbeziers">AddBeziers</a> to add line and Bezier segments. When you are finished adding segments, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure">EndFigure</a> method. You can repeat this sequence to create additional figures. When you are finished creating figures, call the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close">Close</a> method.

To create geometry paths that can contain arcs and quadratic Bezier curves, use an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>.

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink">ID2D1GeometrySink</a>



<a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a>

