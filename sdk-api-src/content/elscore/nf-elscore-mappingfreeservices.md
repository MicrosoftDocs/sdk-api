---
UID: NF:elscore.MappingFreeServices
title: MappingFreeServices function (elscore.h)
description: Frees memory and resources allocated for the application to interact with one or more ELS services. The memory and resources are allocated in an application call to MappingGetServices.
helpviewer_keywords: ["MappingFreeServices","MappingFreeServices function [Internationalization for Windows Applications]","elscore/MappingFreeServices","intl.mappingfreeservices"]
old-location: intl\mappingfreeservices.htm
tech.root: Intl
ms.assetid: 3b90c1c5-3007-4c5d-a51b-e77b1f9c2dd0
ms.date: 12/05/2018
ms.keywords: MappingFreeServices, MappingFreeServices function [Internationalization for Windows Applications], elscore/MappingFreeServices, intl.mappingfreeservices
req.header: elscore.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MappingFreeServices
 - elscore/MappingFreeServices
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Elscore.dll
 - ext-ms-win-els-elscore-l1-1-0.dll
api_name:
 - MappingFreeServices
---

# MappingFreeServices function


## -description

Frees memory and resources allocated for the application to interact with one or more ELS services. The memory and resources are allocated in an application call to <a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>.

## -parameters

### -param pServiceInfo [in]

Pointer to an array of <a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a> structures containing service descriptions retrieved by a prior call to <a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>. This parameter cannot be set to <b>NULL</b>.

## -returns

Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.

## -remarks

<div class="alert"><b>Caution</b>  Services should not be freed before freeing the property bags produced by those services.</div>
<div> </div>
Since all services currently run in the application process, the ELS platform does not unload the service DLLs when the services are released. The operating system unloads the DLLs automatically when the application terminates.

## -see-also

<a href="/windows/desktop/Intl/enumerating-and-freeing-services">Enumerating and Freeing Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappinggetservices">MappingGetServices</a>