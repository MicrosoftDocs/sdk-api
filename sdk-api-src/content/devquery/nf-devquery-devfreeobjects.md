---
UID: NF:devquery.DevFreeObjects
tech.root: devinst
title: DevFreeObjects
ms.date: 11/06/2024
targetos: Windows
description: Frees DEV_OBJECT structures allocated by a call to DevGetObjects or DevGetObjectsEx.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: Cfgmgr32.dll
req.header: devquery.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: Onecore.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 1809
req.target-min-winversvr: Windows Server 2019
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - api-ms-win-devices-query-l1-1-1.dll
 - api-ms-win-devices-query-l1-1-0.dll
 - Cfgmgr32.dll
api_name:
 - DevFreeObjects
f1_keywords:
 - DevFreeObjects
 - devquery/DevFreeObjects
dev_langs:
 - c++
helpviewer_keywords:
 - DevFreeObjects
---

## -description

Frees [DEV_OBJECT](../devquerydef/ns-devquerydef-dev_object.md) structures allocated by a call to [DevGetObjects](nf-devquery-devgetobjects.md) or [DevGetObjectsEx](nf-devquery-devgetobjectsex.md).

## -parameters

### -param cObjectCount [in]

Supplies the number of objects pointed at by *pObjects*.

### -param pObjects [in]

An array of **DEV_OBJECT** structures to be freed.

## -remarks

## -see-also

