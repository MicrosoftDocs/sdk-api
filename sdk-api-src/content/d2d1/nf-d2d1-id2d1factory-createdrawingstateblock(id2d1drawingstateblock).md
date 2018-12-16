---
UID: NF:d2d1.ID2D1Factory.CreateDrawingStateBlock(ID2D1DrawingStateBlock)
title: ID2D1Factory::CreateDrawingStateBlock(ID2D1DrawingStateBlock)
author: windows-sdk-content
description: Creates an ID2D1DrawingStateBlock that can be used with the SaveDrawingState and RestoreDrawingState methods of a render target.
old-location: direct2d\ID2D1Factory_CreateDrawingStateBlock_ptr_ptr_ID2D1DrawingStateBlock.htm
tech.root: direct2d
ms.assetid: 933f10b6-1af6-491a-b030-e04208e79f3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateDrawingStateBlock, CreateDrawingStateBlock method [Direct2D], CreateDrawingStateBlock method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDrawingStateBlock method, ID2D1Factory.CreateDrawingStateBlock, ID2D1Factory.CreateDrawingStateBlock(ID2D1DrawingStateBlock), ID2D1Factory::CreateDrawingStateBlock, ID2D1Factory::CreateDrawingStateBlock(ID2D1DrawingStateBlock), d2d1/ID2D1Factory::CreateDrawingStateBlock, direct2d.ID2D1Factory_CreateDrawingStateBlock_ptr_ptr_ID2D1DrawingStateBlock
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

# ID2D1Factory::CreateDrawingStateBlock(ID2D1DrawingStateBlock)


## -description


Creates an <a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a> that can be used with the <a href="https://msdn.microsoft.com/8658cdbf-979c-41e2-b180-eb21ad6b63c7">SaveDrawingState</a> and <a href="https://msdn.microsoft.com/5b627710-8507-460e-bdc7-2a5633ce370f">RestoreDrawingState</a> methods of a render target.


## -parameters




### -param drawingStateBlock [out]

Type: <b><a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>**</b>

When this method returns, contains the address of a pointer to the new drawing state block created by this method.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>
 

 

