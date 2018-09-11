---
UID: NF:dwrite.IDWriteFactory.CreateMonitorRenderingParams
title: IDWriteFactory::CreateMonitorRenderingParams
author: windows-sdk-content
description: Creates a rendering parameters object with default settings for the specified monitor. In most cases, this is the preferred way to create a rendering parameters object.
old-location: directwrite\IDWriteFactory_CreateMonitorRenderingParams.htm
tech.root: DirectWrite
ms.assetid: ddb6839a-9033-423a-a3f0-9352ec03e440
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: CreateMonitorRenderingParams, CreateMonitorRenderingParams method [Direct Write], CreateMonitorRenderingParams method [Direct Write],IDWriteFactory interface, IDWriteFactory interface [Direct Write],CreateMonitorRenderingParams method, IDWriteFactory.CreateMonitorRenderingParams, IDWriteFactory::CreateMonitorRenderingParams, directwrite.IDWriteFactory_CreateMonitorRenderingParams, dwrite/IDWriteFactory::CreateMonitorRenderingParams
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
 - IDWriteFactory.CreateMonitorRenderingParams
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFactory::CreateMonitorRenderingParams


## -description


 Creates a rendering parameters object with default settings for the specified monitor.
    In most cases, this is the preferred way to create a rendering parameters object.


## -parameters




### -param monitor

Type: <b>HMONITOR</b>

A handle for the specified monitor.


### -param renderingParams [out]

Type: <b><a href="https://msdn.microsoft.com/28b118e4-9a63-46cf-8ab7-e1039126405b">IDWriteRenderingParams</a>**</b>

When this method returns, contains an address of a pointer to the rendering parameters object created by this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>
 

 

