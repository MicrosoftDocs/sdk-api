---
UID: NF:dwrite.IDWriteTextFormat.SetFlowDirection
title: IDWriteTextFormat::SetFlowDirection (dwrite.h)
description: Sets the paragraph flow direction.
helpviewer_keywords: ["IDWriteTextFormat interface [Direct Write]","SetFlowDirection method","IDWriteTextFormat.SetFlowDirection","IDWriteTextFormat::SetFlowDirection","SetFlowDirection","SetFlowDirection method [Direct Write]","SetFlowDirection method [Direct Write]","IDWriteTextFormat interface","directwrite.IDWriteTextFormat_SetFlowDirection","dwrite/IDWriteTextFormat::SetFlowDirection"]
old-location: directwrite\IDWriteTextFormat_SetFlowDirection.htm
tech.root: DirectWrite
ms.assetid: 0eb1648c-b565-46e8-b6db-1fcc6a66b1bd
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetFlowDirection method, IDWriteTextFormat.SetFlowDirection, IDWriteTextFormat::SetFlowDirection, SetFlowDirection, SetFlowDirection method [Direct Write], SetFlowDirection method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetFlowDirection, dwrite/IDWriteTextFormat::SetFlowDirection
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
 - IDWriteTextFormat::SetFlowDirection
 - dwrite/IDWriteTextFormat::SetFlowDirection
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
 - IDWriteTextFormat.SetFlowDirection
---

# IDWriteTextFormat::SetFlowDirection


## -description

 Sets the  paragraph flow direction.

## -parameters

### -param flowDirection

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction">DWRITE_FLOW_DIRECTION</a></b>

The paragraph flow direction; see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction">DWRITE_FLOW_DIRECTION</a> for more information.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

