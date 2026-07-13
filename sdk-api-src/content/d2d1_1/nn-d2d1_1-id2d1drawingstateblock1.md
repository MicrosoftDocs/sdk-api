---
UID: NN:d2d1_1.ID2D1DrawingStateBlock1
title: ID2D1DrawingStateBlock1 (d2d1_1.h)
description: Implementation of a drawing state block that adds the functionality of primitive blend in addition to already existing antialias mode, transform, tags and text rendering mode.
helpviewer_keywords: ["ID2D1DrawingStateBlock1","ID2D1DrawingStateBlock1 interface [Direct2D]","ID2D1DrawingStateBlock1 interface [Direct2D]","described","d2d1_1/ID2D1DrawingStateBlock1","direct2d.id2d1drawingstateblock1"]
old-location: direct2d\id2d1drawingstateblock1.htm
tech.root: Direct2D
ms.assetid: F3A364F6-2C30-4DDE-A5C7-7B58758F111F
ms.date: 12/05/2018
ms.keywords: ID2D1DrawingStateBlock1, ID2D1DrawingStateBlock1 interface [Direct2D], ID2D1DrawingStateBlock1 interface [Direct2D],described, d2d1_1/ID2D1DrawingStateBlock1, direct2d.id2d1drawingstateblock1
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DrawingStateBlock1
 - d2d1_1/ID2D1DrawingStateBlock1
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
 - ID2D1DrawingStateBlock1
---

# ID2D1DrawingStateBlock1 interface


## -description

Implementation of a drawing state block that adds the functionality of primitive blend in addition to already existing antialias mode, transform, tags and text rendering mode.<div class="alert"><b>Note</b>  You can get an <b>ID2D1DrawingStateBlock1</b> using the  <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1factory1-createdrawingstateblock(constd2d1_drawing_state_description1__id2d1drawingstateblock1)">ID2D1Factory::CreateDrawingStateBlock</a> method or you can use the QueryInterface method on an <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a> object.</div>
<div> </div>

## -inheritance

The <b>ID2D1DrawingStateBlock1</b> interface inherits from <a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>. <b>ID2D1DrawingStateBlock1</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-getdescription">ID2D1DrawingStateBlock1::GetDescription1</a>



<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1drawingstateblock1-setdescription">ID2D1DrawingStateBlock1::SetDescription1</a>



<a href="/windows/desktop/Direct2D/id2d1factory-createdrawingstateblock">ID2D1Factory::CreateDrawingStateBlock</a>
