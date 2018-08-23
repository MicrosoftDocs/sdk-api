---
UID: NF:dwrite.IDWriteFactory.GetGdiInterop
title: IDWriteFactory::GetGdiInterop
author: windows-sdk-content
description: Creates an object that is used for interoperability with GDI.
old-location: directwrite\IDWriteFactory_GetGdiInterop.htm
old-project: DirectWrite
ms.assetid: 0ff7930b-8840-42d6-b52d-6766deab1aac
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetGdiInterop, GetGdiInterop method [Direct Write], GetGdiInterop method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],GetGdiInterop method, IDWriteFactory.GetGdiInterop, IDWriteFactory::GetGdiInterop, directwrite.IDWriteFactory_GetGdiInterop, dwrite/IDWriteFactory::GetGdiInterop
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
 - IDWriteFactory.GetGdiInterop
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFactory::GetGdiInterop


## -description


 Creates an object that is used for interoperability with GDI.


## -parameters




### -param gdiInterop [out]

Type: <b><a href="https://msdn.microsoft.com/79472021-ee12-45dd-a943-3908c9e06cde">IDWriteGdiInterop</a>**</b>

When this method returns, contains an address of a pointer to a GDI interop object if successful, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

