---
UID: NS:tdh._TRACE_PROVIDER_INFO
title: TRACE_PROVIDER_INFO (tdh.h)
author: windows-sdk-content
description: Defines the GUID and name for a provider.
old-location: etw\trace_provider_info_struct.htm
tech.root: ETW
ms.assetid: 0dbfde78-b1d4-4cc6-99aa-81de3f647cdb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTRACE_PROVIDER_INFO, TRACE_PROVIDER_INFO, TRACE_PROVIDER_INFO structure [ETW], etw.trace_provider_info_struct, tdh.trace_provider_info_struct, tdh/TRACE_PROVIDER_INFO"
ms.topic: struct
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
 - TRACE_PROVIDER_INFO
product: Windows
targetos: Windows
req.typenames: TRACE_PROVIDER_INFO
req.redist: 
ms.custom: 19H1
---

# TRACE_PROVIDER_INFO structure


## -description


Defines the GUID and name for a provider.


## -struct-fields




### -field ProviderGuid

GUID that uniquely identifies the provider.


### -field SchemaSource

Is zero if the provider uses a XML manifest to provide a description of its events. Otherwise, the value is 1 if the provider uses a WMI MOF class to provide a description of its events.


### -field ProviderNameOffset

Offset to a null-terminated Unicode string that contains the name of the provider. The offset is from the beginning of the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-_provider_enumeration_info">PROVIDER_ENUMERATION_INFO</a> buffer that <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviders">TdhEnumerateProviders</a> returns.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tdh/ns-tdh-_provider_enumeration_info">PROVIDER_ENUMERATION_INFO</a>
 

 

