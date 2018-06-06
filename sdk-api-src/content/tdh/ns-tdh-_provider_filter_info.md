---
UID: NS:tdh._PROVIDER_FILTER_INFO
title: "_PROVIDER_FILTER_INFO"
author: windows-sdk-content
description: Defines a filter and its data.
old-location: etw\provider_filter_info.htm
old-project: ETW
ms.assetid: 0541b24a-8531-4828-8c3b-d889e58b0b38
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPROVIDER_FILTER_INFO, PPROVIDER_FILTER_INFO, PPROVIDER_FILTER_INFO structure pointer [ETW], PROVIDER_FILTER_INFO, PROVIDER_FILTER_INFO structure [ETW], _PROVIDER_FILTER_INFO, etw.provider_filter_info, tdh/PPROVIDER_FILTER_INFO, tdh/PROVIDER_FILTER_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PROVIDER_FILTER_INFO, *PPROVIDER_FILTER_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tdh.h
api_name:
 - PROVIDER_FILTER_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _PROVIDER_FILTER_INFO structure


## -description


Defines a filter and its data.


## -struct-fields




### -field Id

The filter identifier that identifies the filter in the manifest. This is the same value as the <b>value</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field Version

The version number that identifies the version of the filter definition in the manifest. This is the same value as the <b>version</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field MessageOffset

Offset from the beginning of this structure to the message string that describes the filter. This is the same value as the <b>message</b> attribute of the <a href="https://msdn.microsoft.com/f2874b3f-cf3a-4dd9-b914-6adaac33cf7b">FilterType</a> complex type.


### -field Reserved

Reserved.


### -field PropertyCount

The number of elements in the <i>EventPropertyInfoArray</i> array.


### -field EventPropertyInfoArray

An array of <a href="https://msdn.microsoft.com/06b82b31-1f0e-45d5-88ec-9b9835af10df">EVENT_PROPERTY_INFO</a> structures that define the filter data.


## -see-also




<a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a>
 

 

