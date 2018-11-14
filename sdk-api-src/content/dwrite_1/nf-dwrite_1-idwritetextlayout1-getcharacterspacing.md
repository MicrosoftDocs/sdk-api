---
UID: NF:dwrite_1.IDWriteTextLayout1.GetCharacterSpacing
title: IDWriteTextLayout1::GetCharacterSpacing
author: windows-sdk-content
description: Gets the spacing between characters.
old-location: directwrite\idwritetextlayout1_getcharacterspacing.htm
tech.root: DirectWrite
ms.assetid: A546DCB4-8068-4300-94FB-A5B314536869
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: GetCharacterSpacing, GetCharacterSpacing method [Direct Write], GetCharacterSpacing method [Direct Write],IDWriteTextLayout1 interface, IDWriteTextLayout1 interface [Direct Write],GetCharacterSpacing method, IDWriteTextLayout1.GetCharacterSpacing, IDWriteTextLayout1::GetCharacterSpacing, directwrite.idwritetextlayout1_getcharacterspacing, dwrite_1/IDWriteTextLayout1::GetCharacterSpacing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextLayout1.GetCharacterSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_1.h
: 
- IDWriteTextLayout1.GetCharacterSpacing
: 
---

# IDWriteTextLayout1::GetCharacterSpacing


## -description


Gets the spacing between characters.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The current text position.


### -param leadingSpacing [out]

Type: <b>FLOAT*</b>

The spacing before each character, in reading order.


### -param trailingSpacing [out]

Type: <b>FLOAT*</b>

The spacing after each character, in reading order.


### -param minimumAdvanceWidth [out]

Type: <b>FLOAT*</b>

The minimum advance of each character, to prevent characters from becoming too thin or zero-width. This must be zero or greater.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The position range of the current format.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/FF6B3C78-0CC0-4843-9D17-3CF0777EA8BA">IDWriteTextLayout1</a>
 

 

