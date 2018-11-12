---
UID: NF:dwrite.IDWriteTextLayout.SetTypography
title: IDWriteTextLayout::SetTypography
author: windows-sdk-content
description: Sets font typography features for text within a specified text range.
old-location: directwrite\IDWriteTextLayout_SetTypography.htm
tech.root: DirectWrite
ms.assetid: ee0702fb-a3ff-442b-bd3b-6ff35fcba0ec
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetTypography method, IDWriteTextLayout.SetTypography, IDWriteTextLayout::SetTypography, SetTypography, SetTypography method [Direct Write], SetTypography method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetTypography, dwrite/IDWriteTextLayout::SetTypography
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
 - IDWriteTextLayout.SetTypography
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetTypography


## -description


 Sets  font typography features for text within a specified text range.


## -parameters




### -param typography

Type: <b><a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>*</b>

Pointer to font typography settings. 


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

