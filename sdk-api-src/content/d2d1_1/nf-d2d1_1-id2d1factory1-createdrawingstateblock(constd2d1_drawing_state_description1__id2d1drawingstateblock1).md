---
UID: NF:d2d1_1.ID2D1Factory1.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &,ID2D1DrawingStateBlock1)
title: ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &,ID2D1DrawingStateBlock1) (d2d1_1.h)
description: Creates a new drawing state block, this can be used in subsequent SaveDrawingState and RestoreDrawingState operations on the render target.helpviewer_keywords: ["CreateDrawingStateBlock","CreateDrawingStateBlock method [Direct2D]","CreateDrawingStateBlock method [Direct2D]","ID2D1Factory1 interface","ID2D1Factory1 interface [Direct2D]","CreateDrawingStateBlock method","ID2D1Factory1.CreateDrawingStateBlock","ID2D1Factory1.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &","ID2D1DrawingStateBlock1)","ID2D1Factory1::CreateDrawingStateBlock","ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &","ID2D1DrawingStateBlock1)","d2d1_1/ID2D1Factory1::CreateDrawingStateBlock","direct2d.id2d1factory1_createdrawingstateblock2"]
old-location: direct2d\id2d1factory1_createdrawingstateblock2.htm
tech.root: Direct2D
ms.assetid: A7DFF2AD-87CC-4E95-B52D-4C84DAAF469F
ms.date: 12/05/2018
ms.keywords: CreateDrawingStateBlock, CreateDrawingStateBlock method [Direct2D], CreateDrawingStateBlock method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateDrawingStateBlock method, ID2D1Factory1.CreateDrawingStateBlock, ID2D1Factory1.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &,ID2D1DrawingStateBlock1), ID2D1Factory1::CreateDrawingStateBlock, ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &,ID2D1DrawingStateBlock1), d2d1_1/ID2D1Factory1::CreateDrawingStateBlock, direct2d.id2d1factory1_createdrawingstateblock2
f1_keywords:
- d2d1_1/ID2D1Factory1.CreateDrawingStateBlock
dev_langs:
- c++
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
- ID2D1Factory1.CreateDrawingStateBlock
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1 &,ID2D1DrawingStateBlock1)


## -description


Creates a new drawing state block, this can be used in subsequent
          SaveDrawingState and RestoreDrawingState operations on the render target.
        


## -parameters




### -param drawingStateDescription [in, ref, optional]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_drawing_state_description1">D2D1_DRAWING_STATE_DESCRIPTION1</a></b>

The drawing state description structure.


### -param drawingStateBlock [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1drawingstateblock1">ID2D1DrawingStateBlock1</a>**</b>

The address of the newly created drawing state block.


## -returns



Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
            

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.
                </td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid value was passed to the method.</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1">ID2D1Factory1</a>
 

 

