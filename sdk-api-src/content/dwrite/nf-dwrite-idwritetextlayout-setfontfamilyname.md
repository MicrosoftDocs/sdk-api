---
UID: NF:dwrite.IDWriteTextLayout.SetFontFamilyName
title: IDWriteTextLayout::SetFontFamilyName (dwrite.h)
author: windows-sdk-content
description: Sets null-terminated font family name for text within a specified text range.
old-location: directwrite\IDWriteTextLayout_SetFontFamilyName.htm
tech.root: DirectWrite
ms.assetid: c5da17d1-46af-4865-9a6e-a35c6907491b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetFontFamilyName method, IDWriteTextLayout.SetFontFamilyName, IDWriteTextLayout::SetFontFamilyName, SetFontFamilyName, SetFontFamilyName method [Direct Write], SetFontFamilyName method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetFontFamilyName, dwrite/IDWriteTextLayout::SetFontFamilyName
ms.topic: method
f1_keywords: 
 - "dwrite/IDWriteTextLayout.SetFontFamilyName"
dev_langs:
 - c++
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
 - IDWriteTextLayout.SetFontFamilyName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout::SetFontFamilyName


## -description


 Sets null-terminated font family name for text within a specified  text range.


## -parameters




### -param fontFamilyName [in]

Type: <b>const WCHAR*</b>

The font family name that applies to the entire text string within the range specified by <i>textRange</i>.


### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>
 

 

