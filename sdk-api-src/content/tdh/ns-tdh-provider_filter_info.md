---
UID: NS:tdh._PROVIDER_FILTER_INFO
title: PROVIDER_FILTER_INFO (tdh.h)
description: Defines a filter and its data.
helpviewer_keywords: ["*PPROVIDER_FILTER_INFO","PPROVIDER_FILTER_INFO","PPROVIDER_FILTER_INFO structure pointer [ETW]","PROVIDER_FILTER_INFO","PROVIDER_FILTER_INFO structure [ETW]","etw.provider_filter_info","tdh/PPROVIDER_FILTER_INFO","tdh/PROVIDER_FILTER_INFO"]
old-location: etw\provider_filter_info.htm
tech.root: ETW
ms.assetid: 0541b24a-8531-4828-8c3b-d889e58b0b38
ms.date: 12/05/2018
ms.keywords: '*PPROVIDER_FILTER_INFO, PPROVIDER_FILTER_INFO, PPROVIDER_FILTER_INFO structure pointer [ETW], PROVIDER_FILTER_INFO, PROVIDER_FILTER_INFO structure [ETW], etw.provider_filter_info, tdh/PPROVIDER_FILTER_INFO, tdh/PROVIDER_FILTER_INFO'
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PROVIDER_FILTER_INFO, *PPROVIDER_FILTER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROVIDER_FILTER_INFO
 - tdh/_PROVIDER_FILTER_INFO
 - PPROVIDER_FILTER_INFO
 - tdh/PPROVIDER_FILTER_INFO
 - PROVIDER_FILTER_INFO
 - tdh/PROVIDER_FILTER_INFO
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
 - PROVIDER_FILTER_INFO
---

# PROVIDER_FILTER_INFO structure


## -description

Defines a filter and its data.

## -struct-fields

### -field Id

The filter identifier that identifies the filter in the manifest. This is the same value as the <b>value</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-filtertype-complextype">FilterType</a> complex type.

### -field Version

The version number that identifies the version of the filter definition in the manifest. This is the same value as the <b>version</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-filtertype-complextype">FilterType</a> complex type.

### -field MessageOffset

Offset from the beginning of this structure to the message string that describes the filter. This is the same value as the <b>message</b> attribute of the <a href="/windows/desktop/WES/eventmanifestschema-filtertype-complextype">FilterType</a> complex type.

### -field Reserved

Reserved.

### -field PropertyCount

The number of elements in the <i>EventPropertyInfoArray</i> array.

### -field EventPropertyInfoArray

An array of <a href="/windows/desktop/api/tdh/ns-tdh-event_property_info">EVENT_PROPERTY_INFO</a> structures that define the filter data.

## -see-also
<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters">TdhEnumerateProviderFilters</a>