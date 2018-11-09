---
UID: NF:dwrite.IDWriteTextLayout.GetTypography
title: IDWriteTextLayout::GetTypography
author: windows-sdk-content
description: Gets the typography setting of the text at the specified position.
old-location: directwrite\IDWriteTextLayout_GetTypography.htm
tech.root: DirectWrite
ms.assetid: cb7d8bf5-8368-426d-a321-f5c9ef8c7d40
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetTypography, GetTypography method [Direct Write], GetTypography method [Direct Write],IDWriteTextLayout interface, IDWriteTextLayout interface [Direct Write],GetTypography method, IDWriteTextLayout.GetTypography, IDWriteTextLayout::GetTypography, directwrite.IDWriteTextLayout_GetTypography, dwrite/IDWriteTextLayout::GetTypography
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
 - IDWriteTextLayout.GetTypography
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::GetTypography


## -description


 Gets the typography setting of the text at the specified position.


## -parameters




### -param currentPosition

Type: <b>UINT32</b>

The position of the text to inspect.


### -param typography [out]

Type: <b><a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>**</b>

When this method returns, contains an address of a  pointer to the current typography setting.


### -param textRange [out, optional]

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a>*</b>

The range of text that has the same  formatting as the text at the position specified by <i>currentPosition</i>.  This means the run has the exact  formatting as the position specified, including but not limited to the typography.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

