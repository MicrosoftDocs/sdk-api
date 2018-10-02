---
UID: NF:d2d1.ID2D1Factory.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock)
title: ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock)
author: windows-sdk-content
description: Creates an ID2D1DrawingStateBlock that can be used with the SaveDrawingState and RestoreDrawingState methods of a render target.
old-location: direct2d\ID2D1Factory_CreateDrawingStateBlock_ptr_D2D1_DRAWING_STATE_DESCRIPTION_ptr_IDWriteRenderingParams_ptr_ptr_ID2D1DrawingStateBlock.htm
tech.root: direct2d
ms.assetid: d337b0a5-ccd0-42f2-b8c3-0300aa3f2121
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: CreateDrawingStateBlock, CreateDrawingStateBlock method [Direct2D], CreateDrawingStateBlock method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDrawingStateBlock method, ID2D1Factory.CreateDrawingStateBlock, ID2D1Factory.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock), ID2D1Factory::CreateDrawingStateBlock, ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock), d2d1/ID2D1Factory::CreateDrawingStateBlock, direct2d.ID2D1Factory_CreateDrawingStateBlock_ptr_D2D1_DRAWING_STATE_DESCRIPTION_ptr_IDWriteRenderingParams_ptr_ptr_ID2D1DrawingStateBlock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION &,ID2D1DrawingStateBlock)


## -description


Creates an <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a> that can be used with the <a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a> and <a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a> methods of a render target.


## -parameters




### -param drawingStateDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/ba4adc4b-4d86-40c4-8911-1c800d3c6f3e">D2D1_DRAWING_STATE_DESCRIPTION</a>*</b>

A structure that contains antialiasing, transform, and tags  information.


### -param drawingStateBlock [out]

Type: <b><a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>**</b>

When this method returns, contains the address of a pointer to the new drawing state block created by this method.


#### - textRenderingParams [in, optional]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>*</b>

Optional text parameters that indicate how text should be rendered.  


## -returns



Type: <b><a href="a9046ed2-bfb2-4d56-a719-2824afce59ac">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

