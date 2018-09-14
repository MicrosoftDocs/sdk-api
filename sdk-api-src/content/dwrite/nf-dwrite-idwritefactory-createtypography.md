---
UID: NF:dwrite.IDWriteFactory.CreateTypography
title: IDWriteFactory::CreateTypography
author: windows-sdk-content
description: Creates a typography object for use in a text layout.
old-location: directwrite\IDWriteFactory_CreateTypography.htm
tech.root: DirectWrite
ms.assetid: ef6d8289-3a8a-4ec1-89a8-b1b52e311d63
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: CreateTypography, CreateTypography method [Direct Write], CreateTypography method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateTypography method, IDWriteFactory.CreateTypography, IDWriteFactory::CreateTypography, directwrite.IDWriteFactory_CreateTypography, dwrite/IDWriteFactory::CreateTypography
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
 - IDWriteFactory.CreateTypography
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateTypography


## -description


 Creates a typography object for use in a text layout.


## -parameters




### -param typography [out]

Type: <b><a href="https://msdn.microsoft.com/061f42db-e9df-4d8c-981f-68d440dfc4c2">IDWriteTypography</a>**</b>

When this method returns, contains the address of  a pointer to a newly created typography object, or <b>NULL</b> in case of failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

