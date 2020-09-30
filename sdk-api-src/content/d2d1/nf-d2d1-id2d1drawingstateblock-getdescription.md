---
UID: NF:d2d1.ID2D1DrawingStateBlock.GetDescription
title: ID2D1DrawingStateBlock::GetDescription (d2d1.h)
description: Retrieves the antialiasing mode, transform, and tags portion of the drawing state.
helpviewer_keywords: ["GetDescription","GetDescription method [Direct2D]","GetDescription method [Direct2D]","ID2D1DrawingStateBlock interface","ID2D1DrawingStateBlock interface [Direct2D]","GetDescription method","ID2D1DrawingStateBlock.GetDescription","ID2D1DrawingStateBlock::GetDescription","d2d1/ID2D1DrawingStateBlock::GetDescription","direct2d.ID2D1DrawingStateBlock_GetDescription"]
old-location: direct2d\ID2D1DrawingStateBlock_GetDescription.htm
tech.root: Direct2D
ms.assetid: 41c80a2d-0a20-4515-88b0-1878ba6aa945
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Direct2D], GetDescription method [Direct2D],ID2D1DrawingStateBlock interface, ID2D1DrawingStateBlock interface [Direct2D],GetDescription method, ID2D1DrawingStateBlock.GetDescription, ID2D1DrawingStateBlock::GetDescription, d2d1/ID2D1DrawingStateBlock::GetDescription, direct2d.ID2D1DrawingStateBlock_GetDescription
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
 - ID2D1DrawingStateBlock::GetDescription
 - d2d1/ID2D1DrawingStateBlock::GetDescription
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
 - ID2D1DrawingStateBlock.GetDescription
---

# ID2D1DrawingStateBlock::GetDescription


## -description

Retrieves the antialiasing mode, transform, and tags portion of the drawing state.

## -parameters

### -param stateDescription [out]

Type: <b><a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_drawing_state_description">D2D1_DRAWING_STATE_DESCRIPTION</a>*</b>

When this method returns, contains the antialiasing mode, transform, and tags portion of the drawing state. You must allocate storage for this parameter.

## -see-also

<a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_drawing_state_description">D2D1_DRAWING_STATE_DESCRIPTION</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1drawingstateblock">ID2D1DrawingStateBlock</a>

