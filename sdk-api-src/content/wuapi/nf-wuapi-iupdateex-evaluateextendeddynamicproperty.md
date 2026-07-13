---
UID: NF:wuapi.IUpdateEx.EvaluateExtendedDynamicProperty
tech.root: wua
title: IUpdateEx::EvaluateExtendedDynamicProperty
ms.date: 08/13/2024
targetos: Windows
description: Evaluates the value of an extended dynamic property.
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
 - IUpdateEx::EvaluateExtendedDynamicProperty
f1_keywords:
 - IUpdateEx::EvaluateExtendedDynamicProperty
 - wuapi/IUpdateEx::EvaluateExtendedDynamicProperty
dev_langs:
 - c++
helpviewer_keywords:
 - EvaluateExtendedDynamicProperty
---

## -description

Evaluates the value of an extended dynamic property. This value is read-only.

## -parameters

### -param propertyName [in]

The name of the dynamic extended property whose value should be evaluated. The following values are currently supported:

* "DoesUpdateRequireReboot" - Evaluating this attribute requires the update bootstrapper to be downloaded at a minimum.

### -param retval [out]

A pointer to a **VARIANT** that contains the value of the evaluated dynamic property.

## -returns

An **HRESULT** including one of the following values:

| Value | Description |
|-------|-------------|
| S_OK | Success. |
| E_INVALIDARG | The specified property is invalid. |
| WU_E_NOT_SUPPORTED | The specified property is unsupported for reasons such as when the update doesn't contain the required update bootstrapper. |
| WU_E_DM_NOTDOWNLOADED | The update contains an update bootstrapper, but it was not downloaded. |


## -remarks

## -see-also

