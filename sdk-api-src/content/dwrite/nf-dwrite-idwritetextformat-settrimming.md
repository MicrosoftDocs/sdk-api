---
UID: NF:dwrite.IDWriteTextFormat.SetTrimming
title: IDWriteTextFormat::SetTrimming (dwrite.h)
author: windows-sdk-content
description: Sets trimming options for text overflowing the layout width.
old-location: directwrite\IDWriteTextFormat_SetTrimming.htm
tech.root: DirectWrite
ms.assetid: 737eab93-2761-4a59-81e8-ef827be30325
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextFormat interface [Direct Write],SetTrimming method, IDWriteTextFormat.SetTrimming, IDWriteTextFormat::SetTrimming, SetTrimming, SetTrimming method [Direct Write], SetTrimming method [Direct Write],IDWriteTextFormat interface, directwrite.IDWriteTextFormat_SetTrimming, dwrite/IDWriteTextFormat::SetTrimming
ms.topic: method
f1_keywords: ["dwrite/IDWriteTextFormat.SetTrimming"]
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
 - IDWriteTextFormat.SetTrimming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextFormat::SetTrimming


## -description


 Sets trimming options for text overflowing the layout width.


## -parameters




### -param trimmingOptions [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_trimming">DWRITE_TRIMMING</a>*</b>

Text trimming options.


### -param trimmingSign

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a>*</b>

Application-defined omission sign. This parameter may be <b>NULL</b>. See <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwriteinlineobject">IDWriteInlineObject</a> for more information.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>
 

 

