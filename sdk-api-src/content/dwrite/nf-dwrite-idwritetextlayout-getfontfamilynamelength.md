---
UID: NF:dwrite.IDWriteTextLayout.GetFontFamilyNameLength
title: IDWriteTextLayout::GetFontFamilyNameLength
author: windows-sdk-content
description: Get the length of the font family name at the current position.
old-location: directwrite\IDWriteTextLayout_GetFontFamilyNameLength.htm
tech.root: DirectWrite
ms.assetid: e3b3d111-04a7-409b-98dd-b0fc3947f24b
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetFontFamilyNameLength, GetFontFamilyNameLength method [Direct Write], GetFontFamilyNameLength method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontFamilyNameLength method, IDWriteTextLayout.GetFontFamilyNameLength, IDWriteTextLayout::GetFontFamilyNameLength, directwrite.IDWriteTextLayout_GetFontFamilyNameLength, dwrite/IDWriteTextLayout::GetFontFamilyNameLength
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
 - IDWriteTextLayout.GetFontFamilyNameLength
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
- IDWriteTextLayout.GetFontFamilyNameLength
: 
---

# IDWriteTextLayout::GetFontFamilyNameLength


## -description


 Get the length of the font family name at the current position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The current text position.


### -param nameLength [out]

Type: <b>UINT32*</b>

When this method returns, contains the size of the character array containing the font family name, in character count, not including the terminated <b>NULL</b> character.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the font family.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

