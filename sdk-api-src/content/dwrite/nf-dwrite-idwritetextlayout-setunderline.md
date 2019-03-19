---
UID: NF:dwrite.IDWriteTextLayout.SetUnderline
title: IDWriteTextLayout::SetUnderline (dwrite.h)
author: windows-sdk-content
description: Sets underlining for text within a specified text range.
old-location: directwrite\IDWriteTextLayout_SetUnderline.htm
tech.root: DirectWrite
ms.assetid: 677bb4e2-4ae9-4e79-96a3-d4961e317886
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetUnderline method, IDWriteTextLayout.SetUnderline, IDWriteTextLayout::SetUnderline, SetUnderline, SetUnderline method [Direct Write], SetUnderline method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetUnderline, dwrite/IDWriteTextLayout::SetUnderline
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
 - IDWriteTextLayout.SetUnderline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetUnderline


## -description


Sets underlining for text within a specified text range.


## -parameters




### -param hasUnderline

Type: <b>BOOL</b>

A Boolean flag that indicates whether underline takes place within a specified text range.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

