---
UID: NF:d2d1.ID2D1Factory.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock)
title: ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock) (d2d1.h)
description: Creates an ID2D1DrawingStateBlock that can be used with the SaveDrawingState and RestoreDrawingState methods of a render target.helpviewer_keywords: ["CreateDrawingStateBlock","CreateDrawingStateBlock method [Direct2D]","CreateDrawingStateBlock method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateDrawingStateBlock method","ID2D1Factory.CreateDrawingStateBlock","ID2D1Factory.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &","ID2D1DrawingStateBlock)","ID2D1Factory::CreateDrawingStateBlock","ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &","ID2D1DrawingStateBlock)","d2d1/ID2D1Factory::CreateDrawingStateBlock","direct2d.ID2D1Factory_CreateDrawingStateBlock_ref_D2D1_DRAWING_STATE_DESCRIPTION_ptr_ptr_ID2D1DrawingStateBlock"]
old-location: direct2d\ID2D1Factory_CreateDrawingStateBlock_ref_D2D1_DRAWING_STATE_DESCRIPTION_ptr_ptr_ID2D1DrawingStateBlock.htm
tech.root: Direct2D
ms.assetid: 6fd7c199-e2a2-42bb-8227-8d39bae68958
ms.date: 12/05/2018
ms.keywords: CreateDrawingStateBlock, CreateDrawingStateBlock method [Direct2D], CreateDrawingStateBlock method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDrawingStateBlock method, ID2D1Factory.CreateDrawingStateBlock, ID2D1Factory.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock), ID2D1Factory::CreateDrawingStateBlock, ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock), d2d1/ID2D1Factory::CreateDrawingStateBlock, direct2d.ID2D1Factory_CreateDrawingStateBlock_ref_D2D1_DRAWING_STATE_DESCRIPTION_ptr_ptr_ID2D1DrawingStateBlock
f1_keywords:
- d2d1/ID2D1Factory.CreateDrawingStateBlock
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D2d1.dll
api_name:
- ID2D1Factory.CreateDrawingStateBlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock)


## -description


Creates an <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a> that can be used with the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-savedrawingstate">SaveDrawingState</a> and <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-restoredrawingstate">RestoreDrawingState</a> methods of a render target.


## -parameters




### -param drawingStateDescription [ref]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description">D2D1_DRAWING_STATE_DESCRIPTION</a></b>

A structure that contains antialiasing, transform, and tags  information.


### -param drawingStateBlock [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>**</b>

When this method returns, contains the address of a pointer to the new drawing state block created by this method.


## -returns



Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>
 

 

