---
UID: NE:directml.DML_FEATURE_LEVEL
title: DML_FEATURE_LEVEL
description: Defines constants that specify a DirectML *feature level*. A feature level defines a broad umbrella of functionality supported by DirectML.
tech.root: directml
ms.date: 01/19/2022
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
f1_keywords:
 - DML_FEATURE_LEVEL
 - directml/DML_FEATURE_LEVEL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DirectML.h
api_name:
 - DML_FEATURE_LEVEL
---

## -description

Defines constants that specify a DirectML *feature level*. A feature level defines a broad umbrella of functionality supported by DirectML. In using DirectML, you can target specific feature levels, depending on a tradeoff between the level of functionality needed versus the version of DirectML required.

Feature levels in DirectML are strict supersets of one another. This means that every feature level necessarily supports everything that exists in every feature level below (earlier than) it.

For example, `DML_FEATURE_LEVEL_2_0` supports everything that `DML_FEATURE_LEVEL_1_0` does in addition to some new functionality. Similarly, `DML_FEATURE_LEVEL_2_1` supports everything that `DML_FEATURE_LEVEL_2_0` and `DML_FEATURE_LEVEL_1_0` do plus some additional features.

You can specify a *minimum feature level* when creating the DirectML device using [DMLCreateDevice1](/windows/win32/api/directml/nf-directml-dmlcreatedevice1). This has the effect of causing device creation to fail if the underlying DirectML implementation is unable to satisfy the requested feature level. This is useful, for example, if using the system version of DirectML and a user runs your application on an older version of Windows 10.

A DirectML device might support feature levels above the minimum feature level requested through **DMLCreateDevice1**. You can query the device for its supported feature levels using [IDMLDevice::CheckFeatureSupport](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport).

For a list of new capabilities included in each feature level, see [DirectML feature level history](/windows/ai/directml/dml-feature-level-history).

## -enum-fields

### -field DML_FEATURE_LEVEL_1_0:0x1000

Specifies feature level 1_0.

### -field DML_FEATURE_LEVEL_2_0:0x2000

Specifies feature level 2_0.

### -field DML_FEATURE_LEVEL_2_1:0x2100

Specifies feature level 2_1.

### -field DML_FEATURE_LEVEL_3_0:0x3000

Specifies feature level 3_0.

### -field DML_FEATURE_LEVEL_3_1

Specifies feature level 3_1.

### -field DML_FEATURE_LEVEL_4_0

Specifies feature level 4_0.

## -remarks

The **DML_FEATURE_LEVEL_5_0** constant was introduced in `DML_FEATURE_LEVEL_5_0`. **DML_FEATURE_LEVEL_5_0** specifies [feature level 5_0](/windows/ai/directml/dml-feature-level-history#dml_feature_level_5_0).

The **DML_FEATURE_LEVEL_4_1** constant was introduced in `DML_FEATURE_LEVEL_4_1`. **DML_FEATURE_LEVEL_4_1** specifies [feature level 4_1](/windows/ai/directml/dml-feature-level-history#dml_feature_level_4_1).

## Availability

This API was introduced in DirectML version `1.1.0`.

## -see-also

* [DMLCreateDevice1 function](/windows/win32/api/directml/nf-directml-dmlcreatedevice1)
* [IDMLDevice::CheckFeatureSupport method](/windows/win32/api/directml/nf-directml-idmldevice-checkfeaturesupport)
* [DirectML version history](/windows/ai/directml/dml-version-history)
* [DirectML feature level history](/windows/ai/directml/dml-feature-level-history)
