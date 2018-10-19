---
UID: NF:d2d1_1.ID2D1Factory1.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1,IDWriteRenderingParams,ID2D1DrawingStateBlock1)
title: ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1,IDWriteRenderingParams,ID2D1DrawingStateBlock1)
author: windows-sdk-content
description: Creates a new drawing state block, this can be used in subsequent SaveDrawingState and RestoreDrawingState operations on the render target.
old-location: direct2d\id2d1factory1_createdrawingstateblock.htm
tech.root: direct2d
ms.assetid: 1FB96165-3575-4B8B-B8BC-BB94BA5F97CE
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: CreateDrawingStateBlock, CreateDrawingStateBlock method [Direct2D], CreateDrawingStateBlock method [Direct2D],ID2D1Factory1 interface, ID2D1Factory1 interface [Direct2D],CreateDrawingStateBlock method, ID2D1Factory1.CreateDrawingStateBlock, ID2D1Factory1.CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1,IDWriteRenderingParams,ID2D1DrawingStateBlock1), ID2D1Factory1::CreateDrawingStateBlock, ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1,IDWriteRenderingParams,ID2D1DrawingStateBlock1), d2d1_1/ID2D1Factory1::CreateDrawingStateBlock, direct2d.id2d1factory1_createdrawingstateblock
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1Factory1::CreateDrawingStateBlock(const D2D1_DRAWING_STATE_DESCRIPTION1,IDWriteRenderingParams,ID2D1DrawingStateBlock1)


## -description


Creates a new drawing state block, this can be used in subsequent
          SaveDrawingState and RestoreDrawingState operations on the render target.
        


## -parameters




### -param drawingStateDescription [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/E1BFF353-8445-435C-8F7A-E93BFE58A794">D2D1_DRAWING_STATE_DESCRIPTION1</a>*</b>

The drawing state description structure.


### -param textRenderingParams [in, optional]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>*</b>

The DirectWrite rendering params interface.


### -param drawingStateBlock [out]

Type: <b><a href="https://msdn.microsoft.com/F3A364F6-2C30-4DDE-A5C7-7B58758F111F">ID2D1DrawingStateBlock1</a>**</b>

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




<a href="https://msdn.microsoft.com/8221c3b4-e331-403c-9406-ee8d3e103825">ID2D1Factory1</a>
 

 

