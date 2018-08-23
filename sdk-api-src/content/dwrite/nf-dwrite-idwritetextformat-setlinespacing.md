---
UID: NF:dwrite.IDWriteTextFormat.SetLineSpacing
title: IDWriteTextFormat::SetLineSpacing
author: windows-sdk-content
description: Sets the line spacing.
old-location: directwrite\IDWriteTextFormat_SetLineSpacing.htm
old-project: DirectWrite
ms.assetid: 3629779a-5e50-43ea-b161-dd17598b5b43
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetLineSpacing method, IDWriteTextFormat.SetLineSpacing, IDWriteTextFormat::SetLineSpacing, SetLineSpacing, SetLineSpacing method [Direct Write], SetLineSpacing method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetLineSpacing, dwrite/IDWriteTextFormat::SetLineSpacing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextFormat.SetLineSpacing
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteTextFormat::SetLineSpacing


## -description


 Sets the  line spacing.


## -parameters




### -param lineSpacingMethod

Type: <b><a href="https://msdn.microsoft.com/b75e8fee-ed6c-455d-8733-e6972792572c">DWRITE_LINE_SPACING_METHOD</a></b>

Specifies how line height is being determined; see <a href="https://msdn.microsoft.com/b75e8fee-ed6c-455d-8733-e6972792572c">DWRITE_LINE_SPACING_METHOD</a> for more information.


### -param lineSpacing

Type: <b>FLOAT</b>

The line height, or distance between one baseline to another.


### -param baseline

Type: <b>FLOAT</b>

The distance from top of line to baseline. A reasonable ratio to <i>lineSpacing</i> is 80 percent.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



 For the default method, spacing depends solely on the content.
     For uniform spacing, the specified line height overrides the content.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

