---
UID: NF:dwrite.IDWriteTextAnalysisSource.GetTextAtPosition
title: IDWriteTextAnalysisSource::GetTextAtPosition
author: windows-sdk-content
description: Gets a block of text starting at the specified text position.
old-location: directwrite\idwritetextanalysissource_gettextatposition.htm
tech.root: DirectWrite
ms.assetid: d9deabfb-fd0b-4760-a148-b440587654d2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetTextAtPosition, GetTextAtPosition method [Direct Write], GetTextAtPosition method [Direct Write],IDWriteTextAnalysisSource interface, IDWriteTextAnalysisSource interface [Direct Write],GetTextAtPosition method, IDWriteTextAnalysisSource.GetTextAtPosition, IDWriteTextAnalysisSource::GetTextAtPosition, directwrite.idwritetextanalysissource_gettextatposition, dwrite/IDWriteTextAnalysisSource::GetTextAtPosition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextAnalysisSource.GetTextAtPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextAnalysisSource::GetTextAtPosition


## -description


Gets a block of text starting at the specified text position.
     


## -parameters




### -param textPosition

Type: <b>UINT32</b>

The first position of the piece to obtain. All
    positions are in <b>UTF16</b> code units, not whole characters, which
         matters when supplementary characters are used.


### -param textString [out]

Type: <b>const WCHAR**</b>

When this method returns, contains an address of  the block of text as an array of characters to be retrieved from the text analysis.


### -param textLength [out]

Type: <b>UINT32*</b>

When this method returns, contains the number of <b>UTF16</b> units of the retrieved chunk.
         The returned length is not the length of the block, but the length     remaining in the block, from the specified position until its end.
         For example, querying for a position that is 75 positions into a 100-position block would return 25.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Returning <b>NULL</b> indicates the end of text, which is the position after the last character. This function is called iteratively for each consecutive block, tying together several fragmented blocks in the backing store into a virtual contiguous string.

Although applications can implement sparse textual content that  maps only part of the backing store, the application must map any text that is in the range passed to any analysis functions.




## -see-also




<a href="https://msdn.microsoft.com/7e2a523d-9191-4f99-9e73-a7955c432126">IDWriteTextAnalysisSource</a>
 

 

