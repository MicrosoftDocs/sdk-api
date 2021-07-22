---
UID: NF:dwrite.IDWriteTextFormat.SetReadingDirection
title: IDWriteTextFormat::SetReadingDirection (dwrite.h)
description: Sets the paragraph reading direction.
helpviewer_keywords: ["IDWriteTextFormat interface [Direct Write]","SetReadingDirection method","IDWriteTextFormat.SetReadingDirection","IDWriteTextFormat::SetReadingDirection","SetReadingDirection","SetReadingDirection method [Direct Write]","SetReadingDirection method [Direct Write]","IDWriteTextFormat interface","directwrite.IDWriteTextFormat_SetReadingDirection","dwrite/IDWriteTextFormat::SetReadingDirection"]
old-location: directwrite\IDWriteTextFormat_SetReadingDirection.htm
tech.root: DirectWrite
ms.assetid: fb26241c-e97e-43d3-9f0a-0a9f932d8483
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetReadingDirection method, IDWriteTextFormat.SetReadingDirection, IDWriteTextFormat::SetReadingDirection, SetReadingDirection, SetReadingDirection method [Direct Write], SetReadingDirection method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetReadingDirection, dwrite/IDWriteTextFormat::SetReadingDirection
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
 - IDWriteTextFormat::SetReadingDirection
 - dwrite/IDWriteTextFormat::SetReadingDirection
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
 - IDWriteTextFormat.SetReadingDirection
---

# IDWriteTextFormat::SetReadingDirection


## -description

Sets the paragraph reading direction.

## -parameters

### -param readingDirection

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction">DWRITE_READING_DIRECTION</a></b>

The text reading direction (for example, <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction">DWRITE_READING_DIRECTION_RIGHT_TO_LEFT</a> for languages, such as 
            Arabic, that read from right to left) for a paragraph.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The reading direction and flow direction must always be set 90 degrees orthogonal to each other, or else you will get the error DWRITE_E_FLOWDIRECTIONCONFLICTS when you 
        use layout functions like Draw or GetMetrics. So if you set a vertical reading direction (for example, to DWRITE_READING_DIRECTION_TOP_TO_BOTTOM), then you must also 
        use SetFlowDirection to set the flow direction appropriately (for example, to DWRITE_FLOW_DIRECTION_RIGHT_TO_LEFT).

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>

