---
UID: NS:tdh._PROVIDER_FIELD_INFOARRAY
title: PROVIDER_FIELD_INFOARRAY (tdh.h)
description: Defines metadata information about the requested field.
helpviewer_keywords: ["*PPROVIDER_FIELD_INFOARRAY","PROVIDER_FIELD_INFOARRAY","PROVIDER_FIELD_INFOARRAY structure [ETW]","etw.provider_field_infoarray_struct","tdh.provider_field_infoarray_struct","tdh/PROVIDER_FIELD_INFOARRAY"]
old-location: etw\provider_field_infoarray_struct.htm
tech.root: ETW
ms.assetid: c3755ca2-7b17-4f86-9ae8-34621f8b8c1b
ms.date: 12/05/2018
ms.keywords: '*PPROVIDER_FIELD_INFOARRAY, PROVIDER_FIELD_INFOARRAY, PROVIDER_FIELD_INFOARRAY structure [ETW], etw.provider_field_infoarray_struct, tdh.provider_field_infoarray_struct, tdh/PROVIDER_FIELD_INFOARRAY'
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
req.typenames: PROVIDER_FIELD_INFOARRAY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROVIDER_FIELD_INFOARRAY
 - tdh/_PROVIDER_FIELD_INFOARRAY
 - PROVIDER_FIELD_INFOARRAY
 - tdh/PROVIDER_FIELD_INFOARRAY
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
 - PROVIDER_FIELD_INFOARRAY
---

# PROVIDER_FIELD_INFOARRAY structure


## -description

Defines metadata information about the requested field.

## -struct-fields

### -field NumberOfElements

Number of elements in the <b>FieldInfoArray</b> array.

### -field FieldType

Type of field information in  the <b>FieldInfoArray</b> array. For possible values, see the <a href="/windows/desktop/api/tdh/ne-tdh-event_field_type">EVENT_FIELD_TYPE</a> enumeration.

### -field FieldInfoArray

Array of <a href="/windows/desktop/api/tdh/ns-tdh-provider_field_info">PROVIDER_FIELD_INFO</a> structures that define the field's name, description and value.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfieldinformation">TdhEnumerateProviderFieldInformation</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhqueryproviderfieldinformation">TdhQueryProviderFieldInformation</a>