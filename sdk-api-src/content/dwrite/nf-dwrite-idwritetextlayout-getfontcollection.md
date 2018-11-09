---
UID: NF:dwrite.IDWriteTextLayout.GetFontCollection
title: IDWriteTextLayout::GetFontCollection
author: windows-sdk-content
description: Gets the font collection associated with the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetFontCollection.htm
tech.root: DirectWrite
ms.assetid: ce3e4510-2b40-4eb4-aaf8-fe830e96d618
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetFontCollection, GetFontCollection method [Direct Write], GetFontCollection method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetFontCollection method, IDWriteTextLayout.GetFontCollection, IDWriteTextLayout::GetFontCollection, directwrite.IDWriteTextLayout_GetFontCollection, dwrite/IDWriteTextLayout::GetFontCollection
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
 - IDWriteTextLayout.GetFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetFontCollection


## -description


 Gets the font collection associated with the text at the specified position.
    


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.


### -param fontCollection [out]

Type: <b><a href="https://msdn.microsoft.com/2ca7e2d3-d66a-4c57-8fbe-15a5232c3506">IDWriteFontCollection</a>**</b>

Contains an address of a  pointer to the current font collection.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the underline.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

