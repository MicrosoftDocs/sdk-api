---
UID: NF:shdeprecated.IBrowserService.CacheOLEServer
title: IBrowserService::CacheOLEServer
author: windows-sdk-content
description: Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.
old-location: shell\IBrowserService_CacheOLEServer.htm
tech.root: Shell
ms.assetid: 8999e7d7-f29d-4fc8-8f1f-7a8e8b8f45e6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CacheOLEServer, CacheOLEServer method [Windows Shell], CacheOLEServer method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],CacheOLEServer method, IBrowserService.CacheOLEServer, IBrowserService::CacheOLEServer, shdeprecated/IBrowserService::CacheOLEServer, shell.IBrowserService_CacheOLEServer, zone_IBrowserService_CacheOLEServer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.CacheOLEServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
---

# IBrowserService::CacheOLEServer


## -description


Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.


## -parameters




### -param pole [in]

Type: <b><a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/58b32c87-39b6-4d64-9174-cf798ed302c2">IOleObject</a> interface that represents the external object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



