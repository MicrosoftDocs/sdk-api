---
UID: NF:d2d1.ID2D1DrawingStateBlock.GetDescription
title: ID2D1DrawingStateBlock::GetDescription
author: windows-sdk-content
description: Retrieves the antialiasing mode, transform, and tags portion of the drawing state.
old-location: direct2d\ID2D1DrawingStateBlock_GetDescription.htm
tech.root: direct2d
ms.assetid: 41c80a2d-0a20-4515-88b0-1878ba6aa945
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetDescription, GetDescription method [Direct2D], GetDescription method [Direct2D],ID2D1DrawingStateBlock interface, ID2D1DrawingStateBlock interface [Direct2D],GetDescription method, ID2D1DrawingStateBlock.GetDescription, ID2D1DrawingStateBlock::GetDescription, d2d1/ID2D1DrawingStateBlock::GetDescription, direct2d.ID2D1DrawingStateBlock_GetDescription
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
 - ID2D1DrawingStateBlock.GetDescription
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DrawingStateBlock::GetDescription


## -description


Retrieves the antialiasing mode, transform, and tags portion of the drawing state.


## -parameters




### -param stateDescription [out]

Type: <b><a href="https://msdn.microsoft.com/ba4adc4b-4d86-40c4-8911-1c800d3c6f3e">D2D1_DRAWING_STATE_DESCRIPTION</a>*</b>

When this method returns, contains the antialiasing mode, transform, and tags portion of the drawing state. You must allocate storage for this parameter.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/ba4adc4b-4d86-40c4-8911-1c800d3c6f3e">D2D1_DRAWING_STATE_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/9a3d9146-0e1b-4642-ad5d-ff1d09a93d2b">ID2D1DrawingStateBlock</a>
 

 

