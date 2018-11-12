---
UID: NF:dwrite.IDWriteFactory.CreateRenderingParams
title: IDWriteFactory::CreateRenderingParams
author: windows-sdk-content
description: Creates a rendering parameters object with default settings for the primary monitor. Different monitors may have different rendering parameters, for more information see the How to Add Support for Multiple Monitors topic.
old-location: directwrite\IDWriteFactory_CreateRenderingParams.htm
tech.root: DirectWrite
ms.assetid: f5e3e609-62ee-4a0a-aed1-591be852590e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: CreateRenderingParams, CreateRenderingParams method [Direct Write], CreateRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateRenderingParams method, IDWriteFactory.CreateRenderingParams, IDWriteFactory::CreateRenderingParams, directwrite.IDWriteFactory_CreateRenderingParams, dwrite/IDWriteFactory::CreateRenderingParams
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
 - IDWriteFactory.CreateRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateRenderingParams


## -description


 Creates a rendering parameters object with default settings for the primary monitor.
    Different monitors may have different rendering parameters, for more information see the <a href="https://msdn.microsoft.com/62274126-49da-4166-8482-73aac2b29c26">How to Add Support for Multiple Monitors</a> topic.


## -parameters




### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the newly created  rendering parameters object.


## -returns



Type: <b>HRESULT</b>

Standard HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>



<a href="https://msdn.microsoft.com/ddb6839a-9033-423a-a3f0-9352ec03e440">IDWriteFactory::CreateMonitorRenderingParams</a>
 

 

