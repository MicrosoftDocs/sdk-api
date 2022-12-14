---
UID: NE:cfapi.CF_CALLBACK_DEHYDRATION_REASON
tech.root: cloudapi
title: CF_CALLBACK_DEHYDRATION_REASON
ms.date: 03/17/2022
targetos: Windows
description: Specifies the reason why a cloud file was dehydrated.
prerelease: false
req.construct-type: enumeration
req.ddi-compliance: 
req.header: cfapi.h
req.include-header: 
req.kmdf-ver: 
req.max-support: 
req.target-min-winverclnt: Windows 10, version 1709
req.target-min-winversvr: Windows Server 2016
req.target-type: 
req.typenames: 
req.umdf-ver: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - cfapi.h
api_name:
 - CF_CALLBACK_DEHYDRATION_REASON
f1_keywords:
 - CF_CALLBACK_DEHYDRATION_REASON
 - cfapi/CF_CALLBACK_DEHYDRATION_REASON
dev_langs:
 - c++
---

## -description

Specifies the reason why a cloud file was dehydrated.

## -enum-fields

### -field CF_CALLBACK_DEHYDRATION_REASON_NONE

The cloud file has never been dehydrated after its creation.

### -field CF_CALLBACK_DEHYDRATION_REASON_USER_MANUAL

User explicitly dehydrated the cloud file.

### -field CF_CALLBACK_DEHYDRATION_REASON_SYSTEM_LOW_SPACE

The platform dehydrated the cloud file when experiencing low disk space on the volume where this file resides.

### -field CF_CALLBACK_DEHYDRATION_REASON_SYSTEM_INACTIVITY

The platform aged out the cloud file based on user defined policies.

### -field CF_CALLBACK_DEHYDRATION_REASON_SYSTEM_OS_UPGRADE

The platform dehydrated this file when reclaiming disk space in order to upgrade the OS.

## -remarks

## -see-also

