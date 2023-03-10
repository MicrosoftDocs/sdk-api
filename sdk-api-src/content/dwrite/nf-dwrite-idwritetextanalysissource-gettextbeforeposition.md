---
UID: NF:dwrite.IDWriteTextAnalysisSource.GetTextBeforePosition
title: IDWriteTextAnalysisSource::GetTextBeforePosition (dwrite.h)
description: Gets a block of text immediately preceding the specified position.
helpviewer_keywords: ["GetTextBeforePosition","GetTextBeforePosition method [Direct Write]","GetTextBeforePosition method [Direct Write]","IDWriteTextAnalysisSource interface","IDWriteTextAnalysisSource interface [Direct Write]","GetTextBeforePosition method","IDWriteTextAnalysisSource.GetTextBeforePosition","IDWriteTextAnalysisSource::GetTextBeforePosition","directwrite.idwritetextanalysissource_gettextbeforeposition","dwrite/IDWriteTextAnalysisSource::GetTextBeforePosition"]
old-location: directwrite\idwritetextanalysissource_gettextbeforeposition.htm
tech.root: DirectWrite
ms.assetid: af09985b-5f05-47da-be32-cc591fa58765
ms.date: 12/05/2018
ms.keywords: GetTextBeforePosition, GetTextBeforePosition method [Direct Write], GetTextBeforePosition method [Direct Write],IDWriteTextAnalysisSource interface, IDWriteTextAnalysisSource interface [Direct Write],GetTextBeforePosition method, IDWriteTextAnalysisSource.GetTextBeforePosition, IDWriteTextAnalysisSource::GetTextBeforePosition, directwrite.idwritetextanalysissource_gettextbeforeposition, dwrite/IDWriteTextAnalysisSource::GetTextBeforePosition
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
 - IDWriteTextAnalysisSource::GetTextBeforePosition
 - dwrite/IDWriteTextAnalysisSource::GetTextBeforePosition
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
 - IDWriteTextAnalysisSource.GetTextBeforePosition
---

# IDWriteTextAnalysisSource::GetTextBeforePosition


## -description

Gets a block of text immediately preceding the specified position.

## -parameters

### -param textPosition

Type: <b>UINT32</b>

The position immediately after the last position of the block of text to obtain.

### -param textString [out]

Type: <b>const WCHAR**</b>

When this method returns, contains an address of a pointer to the block of text, as an array of characters from the specified range.  The text range will be from <i>textPosition</i> to the front of the block.

### -param textLength [out]

Type: <b>UINT32*</b>

Number of UTF16 units of the retrieved block.
         The length returned is from the specified position to the front of
         the block.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

NULL indicates no chunk available at the specified position, either because <i>textPosition</i> equals 0,  <i>textPosition</i> is greater than the entire text content length, or the queried position is not mapped into the application's backing
     store.

Although applications can implement sparse textual content that  maps only part of
     the backing store, the application must map any text that is in the range passed
     to any analysis functions.

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource">IDWriteTextAnalysisSource</a>

