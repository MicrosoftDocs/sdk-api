---
UID: NE:cfapi.CF_CALLBACK_VALIDATE_DATA_FLAGS
title: CF_CALLBACK_VALIDATE_DATA_FLAGS (cfapi.h)
description: Flags to validate the data of a placeholder file or directory.
helpviewer_keywords: ["CF_CALLBACK_VALIDATE_DATA_FLAGS","CF_CALLBACK_VALIDATE_DATA_FLAGS enumeration","CF_CALLBACK_VALIDATE_DATA_FLAG_EXPLICIT_HYDRATION","CF_CALLBACK_VALIDATE_DATA_FLAG_NONE","cfapi/ CF_CALLBACK_VALIDATE_DATA_FLAG_EXPLICIT_HYDRATION","cfapi/CF_CALLBACK_VALIDATE_DATA_FLAGS","cfapi/CF_CALLBACK_VALIDATE_DATA_FLAG_NONE","cloudApi.cf_callback_validate_data_flags"]
old-location: cloudapi\cf_callback_validate_data_flags.htm
tech.root: cloudapi
ms.assetid: D5BEAEAA-318E-4BA5-8DC5-EDD24E2C26EF
ms.date: 12/05/2018
ms.keywords: CF_CALLBACK_VALIDATE_DATA_FLAGS, CF_CALLBACK_VALIDATE_DATA_FLAGS enumeration, CF_CALLBACK_VALIDATE_DATA_FLAG_EXPLICIT_HYDRATION, CF_CALLBACK_VALIDATE_DATA_FLAG_NONE, cfapi/ CF_CALLBACK_VALIDATE_DATA_FLAG_EXPLICIT_HYDRATION, cfapi/CF_CALLBACK_VALIDATE_DATA_FLAGS, cfapi/CF_CALLBACK_VALIDATE_DATA_FLAG_NONE, cloudApi.cf_callback_validate_data_flags
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
req.typenames: CF_CALLBACK_VALIDATE_DATA_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CF_CALLBACK_VALIDATE_DATA_FLAGS
 - cfapi/CF_CALLBACK_VALIDATE_DATA_FLAGS
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
 - CF_CALLBACK_VALIDATE_DATA_FLAGS
---

# CF_CALLBACK_VALIDATE_DATA_FLAGS enumeration


## -description

Flags to validate the data of a placeholder file or directory.

## -enum-fields

### -field CF_CALLBACK_VALIDATE_DATA_FLAG_NONE:0x00000000

No data validation flag.

### -field CF_CALLBACK_VALIDATE_DATA_FLAG_EXPLICIT_HYDRATION:0x00000002

<b>Note</b>  This value is new for Windows 10, version 1803.

Set if the callback is invoked as a result of a call to <a href="/windows/desktop/api/cfapi/nf-cfapi-cfhydrateplaceholder">CfHydratePlaceholder</a>.
