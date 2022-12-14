---
UID: NF:dwrite.IDWriteTextFormat.GetFlowDirection
title: IDWriteTextFormat::GetFlowDirection (dwrite.h)
description: Gets the direction that text lines flow.
helpviewer_keywords: ["GetFlowDirection","GetFlowDirection method [Direct Write]","GetFlowDirection method [Direct Write]","IDWriteTextFormat interface","IDWriteTextFormat interface [Direct Write]","GetFlowDirection method","IDWriteTextFormat.GetFlowDirection","IDWriteTextFormat::GetFlowDirection","directwrite.IDWriteTextFormat_GetFlowDirection","dwrite/IDWriteTextFormat::GetFlowDirection"]
old-location: directwrite\IDWriteTextFormat_GetFlowDirection.htm
tech.root: DirectWrite
ms.assetid: 993eb17b-a03a-44f7-b273-a0746db3ed70
ms.date: 12/05/2018
ms.keywords: GetFlowDirection, GetFlowDirection method [Direct Write], GetFlowDirection method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetFlowDirection method, IDWriteTextFormat.GetFlowDirection, IDWriteTextFormat::GetFlowDirection, directwrite.IDWriteTextFormat_GetFlowDirection, dwrite/IDWriteTextFormat::GetFlowDirection
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteTextFormat::GetFlowDirection
 - dwrite/IDWriteTextFormat::GetFlowDirection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat.GetFlowDirection
---

# IDWriteTextFormat::GetFlowDirection


## -description

 Gets the direction that text lines flow.



## -returns

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction">DWRITE_FLOW_DIRECTION</a></b>

The direction that text lines flow within their parent container.  For example, <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction">DWRITE_FLOW_DIRECTION_TOP_TO_BOTTOM</a> indicates that text lines are placed from top to bottom.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

