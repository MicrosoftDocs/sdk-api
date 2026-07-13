---
UID: NF:devquery.DevFindProperty
tech.root: devinst
title: DevFindProperty
ms.date: 11/07/2024
targetos: Windows
description: Finds the DEVPROPERTY that corresponds to a particular property within an array of DEVPROPERTY structures.
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
 - DevFindProperty
f1_keywords:
 - DevFindProperty
 - devquery/DevFindProperty
dev_langs:
 - c++
helpviewer_keywords:
 - DevFindProperty
---

## -syntax

```cpp
const DEVPROPERTY* WINAPI DevFindProperty(
    [in] const DEVPROPKEY *pKey,
    [in] DEVPROPSTORE Store,
    [in] PCWSTR pszLocaleName,
    [in] ULONG cProperties,
    [in] const DEVPROPERTY *pProperties);
```

## -description

Finds the [DEVPROPERTY](/windows-hardware/drivers/install/devproperty) that corresponds to a particular property within an array of **DEVPROPERTY** structures.

## -parameters

### -param pKey [in]

A [DEVPROPKEY](/windows-hardware/drivers/install/devpropkey) value identifying the property to find.

### -param Store

The **DEVPROPSTORE** value that indicates the property store of the property to find.

### -param pszLocaleName [in,optional]

The locale name of the property to find. Typically, this will be NULL.

### -param cProperties [in]

The count of elements pointed at by *pProperties*.

### -param pProperties [in]

An array of **DEVPROPERTY** structures to search for the specified property in.

## -returns

A pointer to the **DEVPROPERTY** structure that matches the specified search criteria or NULL if no matching property was found.

## -remarks

## -see-also

