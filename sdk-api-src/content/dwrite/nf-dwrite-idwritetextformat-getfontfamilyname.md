---
UID: NF:dwrite.IDWriteTextFormat.GetFontFamilyName
title: IDWriteTextFormat::GetFontFamilyName
author: windows-sdk-content
description: Gets a copy of the font family name.
old-location: directwrite\IDWriteTextFormat_GetFontFamilyName.htm
tech.root: DirectWrite
ms.assetid: 44d294bf-ec0f-4c75-b10a-2f3e4883b58a
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetFontFamilyName, GetFontFamilyName method [Direct Write], GetFontFamilyName method [Direct Write],IDWriteTextFormat interface, IDWriteTextFormat interface [Direct Write],GetFontFamilyName method, IDWriteTextFormat.GetFontFamilyName, IDWriteTextFormat::GetFontFamilyName, directwrite.IDWriteTextFormat_GetFontFamilyName, dwrite/IDWriteTextFormat::GetFontFamilyName
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
 - IDWriteTextFormat.GetFontFamilyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat::GetFontFamilyName


## -description


 Gets a copy of the font family name.


## -parameters




### -param fontFamilyName [out]

Type: <b>WCHAR*</b>

When this method returns, contains a pointer to a character array, which is null-terminated, that receives the current font family name. The buffer allocated for this array should be at least the size, in elements, of <i>nameSize</i>.


### -param nameSize

Type: <b>UINT32</b>

The size of the <i>fontFamilyName</i> character array, in character count, including the terminated <b>NULL</b> character.  To find the size of <i>fontFamilyName</i>, use <a href="https://msdn.microsoft.com/4bf57fc7-ba5e-44dd-8dd1-47e759842a57">GetFontFamilyNameLength</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

