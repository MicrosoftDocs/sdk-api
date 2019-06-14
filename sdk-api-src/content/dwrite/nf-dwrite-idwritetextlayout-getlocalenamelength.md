---
UID: NF:dwrite.IDWriteTextLayout.GetLocaleNameLength
title: IDWriteTextLayout::GetLocaleNameLength (dwrite.h)
author: windows-sdk-content
description: Gets the length of the locale name of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetLocaleNameLength.htm
tech.root: DirectWrite
ms.assetid: 65d05939-ed51-45e9-a556-71a8cf52b196
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetLocaleNameLength, GetLocaleNameLength method [Direct Write], GetLocaleNameLength method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetLocaleNameLength method, IDWriteTextLayout.GetLocaleNameLength, IDWriteTextLayout::GetLocaleNameLength, directwrite.IDWriteTextLayout_GetLocaleNameLength, dwrite/IDWriteTextLayout::GetLocaleNameLength
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
 - IDWriteTextLayout.GetLocaleNameLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout::GetLocaleNameLength


## -description


 Gets the length of the locale name of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.


### -param nameLength [out]

Type: <b>UINT32*</b>

Size of the character array, in character count, not including the terminated <b>NULL</b> character.


### -param textRange [out, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the locale name.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout">IDWriteTextLayout</a>
 

 

