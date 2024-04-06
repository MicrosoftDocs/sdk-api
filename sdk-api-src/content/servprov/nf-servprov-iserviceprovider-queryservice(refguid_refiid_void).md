---
UID: NF:servprov.IServiceProvider.QueryService(REFGUID,REFIID,void)
tech.root: com
title: IServiceProvider::QueryService(REFGUID,REFIID,void)
ms.date: 07/01/2021
targetos: Windows
description: Acts as the factory method for any services exposed through an implementation of IServiceProvider. Accepts a CLSID parameter.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: servprov.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - servprov.h
api_name:
 - IServiceProvider::QueryService
f1_keywords:
 - IServiceProvider::QueryService
 - servprov/IServiceProvider::QueryService
dev_langs:
 - c++
---

## -description

## -parameters

Acts as the factory method for any services exposed through an implementation of [IServiceProvider](nn-servprov-iserviceprovider.md). Accepts a CLSID parameter.

### -param guidService

The unique identifier of the service (an SID).

### -param riid

The unique identifier of the interface that the caller wants to receive for the service.

### -param ppvObject

The address of the caller-allocated variable to receive the interface pointer of the service on successful return from this function. The caller becomes responsible for calling [Release](../unknwn/nf-unknwn-iunknown-release.md) through this interface pointer when the service is no longer required.

## -returns

S_OK on success.

## -remarks

**QueryService** creates or accesses the implementation of the service identified with guidService. In ppv, it returns the address of the interface that is specified by riid.

## -see-also

