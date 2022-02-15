---
UID: NS:ioringapi.IORING_CAPABILITIES
tech.root: fs
title: IORING_CAPABILITIES
ms.date: 07/16/2021
targetos: Windows
description: Represents the IORING API capabilities.
prerelease: false
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: ioringapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000 
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.typenames: IORING_CAPABILITIES
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - ioringapi.h
api_name:
 - IORING_CAPABILITIES
f1_keywords:
 - IORING_CAPABILITIES
 - ioringapi/IORING_CAPABILITIES
dev_langs:
 - c++
---

## -description

Represents the IORING API capabilities.

## -struct-fields

### -field MaxVersion

A value from the [IORING_VERSION](../ntioring_x/ne-ntioring_x-ioring_version.md) enumeration specifying the maximum supported IORING API version.

### -field MaxSubmissionQueueSize

The maximum submission queue size.

### -field MaxCompletionQueueSize

The maximum completion queue size.

### -field FeatureFlags

A value from the [IORING_FEATURE_FLAGS](../ntioring_x/) enumeration specifying feature flags for the IORING API implementation.

## -remarks

## -see-also

