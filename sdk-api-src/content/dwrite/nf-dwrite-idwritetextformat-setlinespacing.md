---
UID: NF:dwrite.IDWriteTextFormat.SetLineSpacing
title: IDWriteTextFormat::SetLineSpacing (dwrite.h)
author: windows-sdk-content
description: Sets the line spacing.
old-location: directwrite\IDWriteTextFormat_SetLineSpacing.htm
tech.root: DirectWrite
ms.assetid: 3629779a-5e50-43ea-b161-dd17598b5b43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetLineSpacing method, IDWriteTextFormat.SetLineSpacing, IDWriteTextFormat::SetLineSpacing, SetLineSpacing, SetLineSpacing method [Direct Write], SetLineSpacing method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetLineSpacing, dwrite/IDWriteTextFormat::SetLineSpacing
ms.topic: method
f1_keywords: 
 - "dwrite/IDWriteTextFormat.SetLineSpacing"
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
 - IDWriteTextFormat.SetLineSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat::SetLineSpacing


## -description


 Sets the  line spacing.


## -parameters




### -param lineSpacingMethod

Type: <b><a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method">DWRITE_LINE_SPACING_METHOD</a></b>

Specifies how line height is being determined; see <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method">DWRITE_LINE_SPACING_METHOD</a> for more information.


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




<a href="/windows/win32/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>
 

 

