---
UID: NF:dwrite.IDWriteFactory.CreateTextLayout
title: IDWriteFactory::CreateTextLayout
author: windows-sdk-content
description: Takes a string, text format, and associated constraints, and produces an object that represents the fully analyzed and formatted result.
old-location: directwrite\IDWriteFactory_CreateTextLayout.htm
tech.root: DirectWrite
ms.assetid: f76f85df-112f-4bc3-b922-a0d7940d2954
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: CreateTextLayout, CreateTextLayout method [Direct Write], CreateTextLayout method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTextLayout method, IDWriteFactory.CreateTextLayout, IDWriteFactory::CreateTextLayout, directwrite.IDWriteFactory_CreateTextLayout, dwrite/IDWriteFactory::CreateTextLayout
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
 - IDWriteFactory.CreateTextLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateTextLayout


## -description


 Takes a string, text format, and associated constraints,
     and produces an object that represents the fully analyzed
     and formatted result.


## -parameters




### -param string [in]

Type: <b>const WCHAR*</b>

An array of characters that contains the string to create a new <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> object from. This array must be of length <i>stringLength</i> and can contain embedded <b>NULL</b> characters.


### -param stringLength

Type: <b>UINT32</b>

The number of characters in  the string.


### -param textFormat

Type: <b><a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>*</b>

A pointer to an object that indicates the format to apply to the string.


### -param maxWidth

Type: <b>FLOAT</b>

The width of the layout box.


### -param maxHeight

Type: <b>FLOAT</b>

The height of the layout box.


### -param textLayout [out]

Type: <b><a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>**</b>

When this method returns, contains an address of a pointer to the resultant text layout object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

