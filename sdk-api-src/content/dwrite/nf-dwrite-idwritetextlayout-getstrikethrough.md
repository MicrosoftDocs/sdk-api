---
UID: NF:dwrite.IDWriteTextLayout.GetStrikethrough
title: IDWriteTextLayout::GetStrikethrough (dwrite.h)
author: windows-sdk-content
description: Get the strikethrough presence of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetStrikethrough.htm
tech.root: DirectWrite
ms.assetid: 39a1af39-a8b3-47b2-b3cb-8e807ae202c9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStrikethrough, GetStrikethrough method [Direct Write], GetStrikethrough method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetStrikethrough method, IDWriteTextLayout.GetStrikethrough, IDWriteTextLayout::GetStrikethrough, directwrite.IDWriteTextLayout_GetStrikethrough, dwrite/IDWriteTextLayout::GetStrikethrough
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
 - IDWriteTextLayout.GetStrikethrough
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetStrikethrough


## -description


 Get the strikethrough presence of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.


### -param hasStrikethrough [out]

Type: <b>BOOL*</b>

A Boolean  flag that indicates whether strikethrough is present at the position indicated by <i>currentPosition</i>.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

Contains the range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to strikethrough.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

