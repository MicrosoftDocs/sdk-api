---
UID: NF:wuapi.IUpdateEx.get_ExtendedStaticProperty
tech.root: wua
title: IUpdateEx::get_ExtendedStaticProperty
ms.date: 08/13/2024
targetos: Windows
description: Gets the value for the extended property being queried.
prerelease: true
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: wuapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11 Build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - wuapi.h
api_name:
 - IUpdateEx::get_ExtendedStaticProperty
f1_keywords:
 - IUpdateEx::get_ExtendedStaticProperty
 - wuapi/IUpdateEx::get_ExtendedStaticProperty
dev_langs:
 - c++
helpviewer_keywords:
 - get_ExtendedStaticProperty
---

## -description

Gets the value of an extended static property. This value is read-only.

## -parameters

### -param propertyName [in]

The name of the static extended property being queried. The following values are currently supported:

* "ContainsUpdateBootstrapper"

### -param retval [out]

A pointer to a **VARIANT** that contains the value of the queried static property.

## -returns

An **HRESULT** including one of the following values:

| Value | Description |
|-------|-------------|
| S_OK | Success. |
| E_INVALIDARG | The specified property is invalid. |
| WU_E_NOT_SUPPORTED | The specified property or operation is unsupported. |

## -remarks

## -see-also

