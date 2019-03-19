---
UID: NF:dwrite.IDWriteTextLayout.GetFontFamilyName
title: IDWriteTextLayout::GetFontFamilyName (dwrite.h)
author: windows-sdk-content
description: Copies the font family name of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetFontFamilyName.htm
tech.root: DirectWrite
ms.assetid: c5283d1f-8a40-4272-b71c-590b6bc6a340
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetFontFamilyName, GetFontFamilyName method [Direct Write], GetFontFamilyName method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontFamilyName method, IDWriteTextLayout.GetFontFamilyName, IDWriteTextLayout::GetFontFamilyName, directwrite.IDWriteTextLayout_GetFontFamilyName, dwrite/IDWriteTextLayout::GetFontFamilyName
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
 - IDWriteTextLayout.GetFontFamilyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetFontFamilyName


## -description


 Copies the font family name of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to examine.


### -param fontFamilyName [out]

Type: <b>WCHAR*</b>

When this method returns, contains an array of characters that receives the current font family name. You must allocate storage for this parameter.


### -param nameSize

Type: <b>UINT32</b>

The size of the character array in character count including the terminated <b>NULL</b> character.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font family name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

