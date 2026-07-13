---
UID: NS:tdh._PROVIDER_FIELD_INFO
title: PROVIDER_FIELD_INFO (tdh.h)
description: Defines the field information.
helpviewer_keywords: ["*PPROVIDER_FIELD_INFO","PROVIDER_FIELD_INFO","PROVIDER_FIELD_INFO structure [ETW]","etw.provider_field_info_struct","tdh.provider_field_info_struct","tdh/PROVIDER_FIELD_INFO"]
old-location: etw\provider_field_info_struct.htm
tech.root: ETW
ms.assetid: a7c88c25-3acc-42aa-bf2b-bc7651e84f8c
ms.date: 12/05/2018
ms.keywords: '*PPROVIDER_FIELD_INFO, PROVIDER_FIELD_INFO, PROVIDER_FIELD_INFO structure [ETW], etw.provider_field_info_struct, tdh.provider_field_info_struct, tdh/PROVIDER_FIELD_INFO'
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: PROVIDER_FIELD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROVIDER_FIELD_INFO
 - tdh/_PROVIDER_FIELD_INFO
 - PROVIDER_FIELD_INFO
 - tdh/PROVIDER_FIELD_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PROVIDER_FIELD_INFO
---

# PROVIDER_FIELD_INFO structure


## -description

Defines the field information.

## -struct-fields

### -field NameOffset

Offset to the null-terminated Unicode string that contains the name of the field, in English only.

### -field DescriptionOffset

Offset to the null-terminated Unicode string that contains the localized description of the field. The value is zero if the description does not exist.

### -field Value

Field value.

## -see-also
<a href="/windows/desktop/api/tdh/ns-tdh-provider_field_infoarray">PROVIDER_FIELD_INFOARRAY</a>