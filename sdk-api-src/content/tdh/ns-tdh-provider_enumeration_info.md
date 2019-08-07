---
UID: NS:tdh._PROVIDER_ENUMERATION_INFO
title: PROVIDER_ENUMERATION_INFO (tdh.h)
author: windows-sdk-content
description: Defines the array of providers that have registered a MOF or manifest on the computer.
old-location: etw\provider_enumeration_info_struct.htm
tech.root: ETW
ms.assetid: bb4548fb-70e5-4726-bc92-adb7ba7be0e4
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*PPROVIDER_ENUMERATION_INFO, PROVIDER_ENUMERATION_INFO, PROVIDER_ENUMERATION_INFO structure [ETW], etw.provider_enumeration_info_struct, tdh.provider_enumeration_info_struct, tdh/PROVIDER_ENUMERATION_INFO'
ms.topic: struct
f1_keywords:
- tdh/PROVIDER_ENUMERATION_INFO
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Tdh.h
api_name:
- PROVIDER_ENUMERATION_INFO
product: Windows
targetos: Windows
req.typenames: PROVIDER_ENUMERATION_INFO
req.redist: 
ms.custom: 19H1
---

# PROVIDER_ENUMERATION_INFO structure


## -description


Defines the array of providers that have registered a MOF or manifest on the computer.


## -struct-fields




### -field NumberOfProviders

Number of elements in the <b>TraceProviderInfoArray</b> array.


### -field Reserved

 


### -field TraceProviderInfoArray

Array of <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-trace_provider_info">TRACE_PROVIDER_INFO</a> structures that contain information about each provider such as its name and unique identifier.


#### - Padding

Reserved.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviders">TdhEnumerateProviders</a>
 

 

