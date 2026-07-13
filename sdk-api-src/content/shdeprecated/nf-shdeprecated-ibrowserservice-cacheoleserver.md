---
UID: NF:shdeprecated.IBrowserService.CacheOLEServer
title: IBrowserService::CacheOLEServer (shdeprecated.h)
description: Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.
helpviewer_keywords: ["CacheOLEServer","CacheOLEServer method [Windows Shell]","CacheOLEServer method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","CacheOLEServer method","IBrowserService.CacheOLEServer","IBrowserService::CacheOLEServer","shdeprecated/IBrowserService::CacheOLEServer","shell.IBrowserService_CacheOLEServer","zone_IBrowserService_CacheOLEServer"]
old-location: shell\IBrowserService_CacheOLEServer.htm
tech.root: shell
ms.assetid: 8999e7d7-f29d-4fc8-8f1f-7a8e8b8f45e6
ms.date: 12/05/2018
ms.keywords: CacheOLEServer, CacheOLEServer method [Windows Shell], CacheOLEServer method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],CacheOLEServer method, IBrowserService.CacheOLEServer, IBrowserService::CacheOLEServer, shdeprecated/IBrowserService::CacheOLEServer, shell.IBrowserService_CacheOLEServer, zone_IBrowserService_CacheOLEServer
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::CacheOLEServer
 - shdeprecated/IBrowserService::CacheOLEServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.CacheOLEServer
---

# IBrowserService::CacheOLEServer


## -description

Deprecated. Caches a reference to an external object to avoid reloading the server on reuse.

## -parameters

### -param pole [in]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a> interface that represents the external object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.