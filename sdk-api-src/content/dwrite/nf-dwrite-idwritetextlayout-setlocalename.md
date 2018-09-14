---
UID: NF:dwrite.IDWriteTextLayout.SetLocaleName
title: IDWriteTextLayout::SetLocaleName
author: windows-sdk-content
description: Sets the locale name for text within a specified text range.
old-location: directwrite\IDWriteTextLayout_SetLocaleName.htm
tech.root: DirectWrite
ms.assetid: c00d28dc-5338-438f-9046-5ad54e845e9d
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IDWriteTextLayout interface [Direct Write],SetLocaleName method, IDWriteTextLayout.SetLocaleName, IDWriteTextLayout::SetLocaleName, SetLocaleName, SetLocaleName method [Direct Write], SetLocaleName method [Direct Write],IDWriteTextLayout interface, directwrite.IDWriteTextLayout_SetLocaleName, dwrite/IDWriteTextLayout::SetLocaleName
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
 - IDWriteTextLayout.SetLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout::SetLocaleName


## -description


 Sets the locale name for text
    within a specified text range.


## -parameters




### -param localeName [in]

Type: <b>const WCHAR*</b>

A null-terminated locale name string.


### -param textRange

Type: <b><a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a>
 

 

