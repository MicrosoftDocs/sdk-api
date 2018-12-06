---
UID: NF:dwrite.IDWriteFactory.CreateTextFormat
title: IDWriteFactory::CreateTextFormat
author: windows-sdk-content
description: Creates a text format object used for text layout.
old-location: directwrite\IDWriteFactory_CreateTextFormat.htm
tech.root: DirectWrite
ms.assetid: d6e7caba-5cba-4b6e-b146-10aa6d21cac1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateTextFormat, CreateTextFormat method [Direct Write], CreateTextFormat method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextFormat method, IDWriteFactory.CreateTextFormat, IDWriteFactory::CreateTextFormat, directwrite.IDWriteFactory_CreateTextFormat, dwrite/IDWriteFactory::CreateTextFormat
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
 - IDWriteFactory.CreateTextFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateTextFormat


## -description


 Creates a text format object used for text layout.


## -parameters




### -param fontFamilyName [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the name of the font family


### -param fontCollection

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>*</b>

A pointer to a font collection object. When this is <b>NULL</b>, indicates the system font collection.


### -param fontWeight

Type: <b><a href="https://msdn.microsoft.com/82396f80-eb62-4865-ba07-9653220c84f2">DWRITE_FONT_WEIGHT</a></b>

A value that indicates the font weight for the text object created by this method.


### -param fontStyle

Type: <b><a href="https://msdn.microsoft.com/e48a3b82-4a60-472d-8cb8-a6f63d7eeefc">DWRITE_FONT_STYLE</a></b>

A value that indicates the font style for the text object created by this method.


### -param fontStretch

Type: <b><a href="https://msdn.microsoft.com/10b3a703-239b-4fb1-9a20-e466b123b060">DWRITE_FONT_STRETCH</a></b>

A value that indicates the font stretch for the text object created by this method.


### -param fontSize

Type: <b>FLOAT</b>

The logical size of the font in DIP ("device-independent pixel") units. A DIP equals 1/96 inch.


### -param localeName [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the locale name.


### -param textFormat [out]

Type: <b><a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>**</b>

When this method returns, contains an address of a pointer to a  newly created text format object, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

