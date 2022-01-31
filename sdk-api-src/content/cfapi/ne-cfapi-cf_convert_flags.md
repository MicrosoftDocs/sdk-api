---
UID: NE:cfapi.CF_CONVERT_FLAGS
title: CF_CONVERT_FLAGS (cfapi.h)
description: Normal file/directory to placeholder file/directory conversion flags.
helpviewer_keywords: ["CF_CONVERT_FLAGS","CF_CONVERT_FLAGS enumeration","CF_CONVERT_FLAG_DEHYDRATE","CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION","CF_CONVERT_FLAG_MARK_IN_SYNC","CF_CONVERT_FLAG_NONE","cfapi/CF_CONVERT_FLAGS","cfapi/CF_CONVERT_FLAG_DEHYDRATE","cfapi/CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION","cfapi/CF_CONVERT_FLAG_MARK_IN_SYNC","cfapi/CF_CONVERT_FLAG_NONE","cloudApi.cf_convert_flags"]
old-location: cloudapi\cf_convert_flags.htm
tech.root: cloudapi
ms.assetid: 0342BF0B-509A-4F8D-9557-54E534A3DDFE
ms.date: 12/05/2018
ms.keywords: CF_CONVERT_FLAGS, CF_CONVERT_FLAGS enumeration, CF_CONVERT_FLAG_DEHYDRATE, CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, CF_CONVERT_FLAG_MARK_IN_SYNC, CF_CONVERT_FLAG_NONE, cfapi/CF_CONVERT_FLAGS, cfapi/CF_CONVERT_FLAG_DEHYDRATE, cfapi/CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION, cfapi/CF_CONVERT_FLAG_MARK_IN_SYNC, cfapi/CF_CONVERT_FLAG_NONE, cloudApi.cf_convert_flags
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
req.typenames: CF_CONVERT_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CONVERT_FLAGS
 - cfapi/CF_CONVERT_FLAGS
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
 - CF_CONVERT_FLAGS
---

# CF_CONVERT_FLAGS enumeration


## -description

Normal file/directory to placeholder file/directory conversion flags.

## -enum-fields

### -field CF_CONVERT_FLAG_NONE:0x00000000

No conversion flags.

### -field CF_CONVERT_FLAG_MARK_IN_SYNC:0x00000001

The platform marks the converted placeholder as in sync with cloud upon a successful conversion of the file.

### -field CF_CONVERT_FLAG_DEHYDRATE:0x00000002

Applicable to files only. When specified, the platform dehydrates the file after converting it to a placeholder successfully. The caller must acquire an exclusive handle when specifying this flag or data corruptions can occur. Note that the platform does not validate the exclusiveness of the handle.

### -field CF_CONVERT_FLAG_ENABLE_ON_DEMAND_POPULATION:0x00000004

Applicable for directories only. When specified, it marks the converted placeholder directory as partially populated such that any future access to it will result in a FETCH_PLACEHOLDERS callback sent to the sync provider.

