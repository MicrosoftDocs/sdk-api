---
UID: NE:cfapi.CF_PLACEHOLDER_RANGE_INFO_CLASS
title: CF_PLACEHOLDER_RANGE_INFO_CLASS (cfapi.h)
description: Types of the range of placeholder file data.
helpviewer_keywords: ["CF_PLACEHOLDER_RANGE_INFO_CLASS","CF_PLACEHOLDER_RANGE_INFO_CLASS enumeration","CF_PLACEHOLDER_RANGE_INFO_MODIFIED","CF_PLACEHOLDER_RANGE_INFO_ONDISK","CF_PLACEHOLDER_RANGE_INFO_VALIDATED","PCF_PLACEHOLDER_RANGE_INFO_CLASS","PCF_PLACEHOLDER_RANGE_INFO_CLASS enumeration pointer","cfapi/CF_PLACEHOLDER_RANGE_INFO_CLASS","cfapi/CF_PLACEHOLDER_RANGE_INFO_MODIFIED","cfapi/CF_PLACEHOLDER_RANGE_INFO_ONDISK","cfapi/CF_PLACEHOLDER_RANGE_INFO_VALIDATED","cfapi/PCF_PLACEHOLDER_RANGE_INFO_CLASS","cloudApi._cf_placeholder_range_info_class"]
old-location: cloudapi\_cf_placeholder_range_info_class.htm
tech.root: cloudapi
ms.assetid: 04533C98-894C-422F-9BE5-F2746BF13567
ms.date: 12/05/2018
ms.keywords: CF_PLACEHOLDER_RANGE_INFO_CLASS, CF_PLACEHOLDER_RANGE_INFO_CLASS enumeration, CF_PLACEHOLDER_RANGE_INFO_MODIFIED, CF_PLACEHOLDER_RANGE_INFO_ONDISK, CF_PLACEHOLDER_RANGE_INFO_VALIDATED, PCF_PLACEHOLDER_RANGE_INFO_CLASS, PCF_PLACEHOLDER_RANGE_INFO_CLASS enumeration pointer, cfapi/CF_PLACEHOLDER_RANGE_INFO_CLASS, cfapi/CF_PLACEHOLDER_RANGE_INFO_MODIFIED, cfapi/CF_PLACEHOLDER_RANGE_INFO_ONDISK, cfapi/CF_PLACEHOLDER_RANGE_INFO_VALIDATED, cfapi/PCF_PLACEHOLDER_RANGE_INFO_CLASS, cloudApi._cf_placeholder_range_info_class
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_PLACEHOLDER_RANGE_INFO_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_PLACEHOLDER_RANGE_INFO_CLASS
 - cfapi/CF_PLACEHOLDER_RANGE_INFO_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CfApi.h
api_name:
 - CF_PLACEHOLDER_RANGE_INFO_CLASS
---

# CF_PLACEHOLDER_RANGE_INFO_CLASS enumeration


## -description

Types of the range of placeholder file data.

## -enum-fields

### -field CF_PLACEHOLDER_RANGE_INFO_ONDISK:1

On-disk data is data that is physical present in the file, which is a super set of other types of ranges.

### -field CF_PLACEHOLDER_RANGE_INFO_VALIDATED:2

Validated data is a subset of the on-disk data that is currently in sync with the cloud.

### -field CF_PLACEHOLDER_RANGE_INFO_MODIFIED:3

Modified data is a subset of the on-disk data that is currently not in sync with the cloud, i.e., either modified or appended.

