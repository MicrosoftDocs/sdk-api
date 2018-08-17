---
UID: NS:tdh._PROVIDER_ENUMERATION_INFO
title: "_PROVIDER_ENUMERATION_INFO"
author: windows-sdk-content
description: Defines the array of providers that have registered a MOF or manifest on the computer.
old-location: etw\provider_enumeration_info_struct.htm
old-project: etw
ms.assetid: bb4548fb-70e5-4726-bc92-adb7ba7be0e4
ms.author: windowssdkdev
ms.date: 08/08/2018
ms.keywords: "*PPROVIDER_ENUMERATION_INFO, PROVIDER_ENUMERATION_INFO, PROVIDER_ENUMERATION_INFO structure [ETW], _PROVIDER_ENUMERATION_INFO, etw.provider_enumeration_info_struct, tdh.provider_enumeration_info_struct, tdh/PROVIDER_ENUMERATION_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: tdh.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PROVIDER_ENUMERATION_INFO
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
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _PROVIDER_ENUMERATION_INFO structure


## -description


Defines the array of providers that have registered a MOF or manifest on the computer.


## -struct-fields




### -field NumberOfProviders

Number of elements in the <b>TraceProviderInfoArray</b> array.


### -field Reserved

 


### -field TraceProviderInfoArray

Array of <a href="https://msdn.microsoft.com/0dbfde78-b1d4-4cc6-99aa-81de3f647cdb">TRACE_PROVIDER_INFO</a> structures that contain information about each provider such as its name and unique identifier.


#### - Padding

Reserved.


## -see-also




<a href="https://msdn.microsoft.com/ef326ef8-227d-46b5-88b9-b519748fb778">TdhEnumerateProviders</a>
 

 

