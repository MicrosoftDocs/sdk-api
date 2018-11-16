---
UID: NF:dwrite.IDWriteFactory.CreateGdiCompatibleTextLayout
title: IDWriteFactory::CreateGdiCompatibleTextLayout
author: windows-sdk-content
description: Takes a string, format, and associated constraints, and produces an object representing the result, formatted for a particular display resolution and measuring mode.
old-location: directwrite\IDWriteFactory_CreateDisplayTextLayout.htm
tech.root: DirectWrite
ms.assetid: f9205ce6-1586-461a-9c48-3f3f25780dd0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CreateGdiCompatibleTextLayout, CreateGdiCompatibleTextLayout method [Direct Write], CreateGdiCompatibleTextLayout method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateGdiCompatibleTextLayout method, IDWriteFactory.CreateGdiCompatibleTextLayout, IDWriteFactory::CreateGdiCompatibleTextLayout, directwrite.IDWriteFactory_CreateDisplayTextLayout, dwrite/IDWriteFactory::CreateGdiCompatibleTextLayout
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
 - IDWriteFactory.CreateGdiCompatibleTextLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteFactory.CreateGdiCompatibleTextLayout
: 
---

# IDWriteFactory::CreateGdiCompatibleTextLayout


## -description


 Takes a string, format, and associated constraints,
     and produces an object representing the result, formatted for a particular display resolution
     and measuring mode. 


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the string to create a new <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> object from. This array must be of length <i>stringLength</i> and can contain embedded <b>NULL</b> characters.


### -param stringLength

Type: <b>UINT32</b>

The length of the string, in character count.


### -param textFormat

Type: <b><a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>*</b>

The text formatting object to apply to the string.


### -param layoutWidth

Type: <b>FLOAT</b>

The width of the layout box.


### -param layoutHeight

Type: <b>FLOAT</b>

The height of the layout box.


### -param pixelsPerDip

Type: <b>FLOAT</b>

The number of physical pixels per DIP (device independent pixel). For example, if rendering onto a 96 DPI device <i>pixelsPerDip</i>is 1. If rendering onto a 120 DPI device <i>pixelsPerDip</i> is 1.25 (120/96).


### -param transform [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/fe4bd8ba-fc3b-4a04-8a72-9983d52f4404">DWRITE_MATRIX</a>*</b>

An optional transform applied to the glyphs and their positions. This transform is applied after the
     scaling specifies the font size and pixels per DIP.


### -param useGdiNatural

Type: <b>BOOL</b>

 Instructs the text layout to use the same metrics as GDI bi-level text when set to <b>FALSE</b>.
     When set to <b>TRUE</b>, instructs the text layout to use the same metrics as text measured by GDI using a font
     created with <b>CLEARTYPE_NATURAL_QUALITY</b>.


### -param textLayout [out]

Type: <b><a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>**</b>

When this method returns, contains an address to the pointer of the resultant text layout object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The resulting text layout should only be used for the intended resolution,
     and for cases where text scalability is desired <a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">CreateTextLayout</a> should be used instead.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

