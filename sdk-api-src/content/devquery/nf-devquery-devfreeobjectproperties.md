---
UID: NF:devquery.DevFreeObjectProperties
tech.root: devinst
title: DevFreeObjectProperties
ms.date: 11/07/2025
targetos: Windows
description: Frees DEVPROPERTY structures allocated by calls to DevGetObjectProperties or DevGetObjectPropertiesEx.
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
 - DevFreeObjectProperties
f1_keywords:
 - DevFreeObjectProperties
 - devquery/DevFreeObjectProperties
dev_langs:
 - c++
helpviewer_keywords:
 - DevFreeObjectProperties
---

## -description

Frees [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) structures allocated by calls to [DevGetObjectProperties](nf-devquery-devgetobjectproperties.md) or [DevGetObjectPropertiesEx](nf-devquery-devgetobjectpropertiesex.md).

## -parameters

### -param cPropertyCount [in]

Supplies the number of elements pointed at by *pProperties*.

### -param pProperties [in]

An array of [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) structures to be freed.

## -remarks

## -see-also

