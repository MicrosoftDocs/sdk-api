---
UID: NF:elscore.MappingGetServices
title: MappingGetServices function (elscore.h)
description: Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.
helpviewer_keywords: ["MappingGetServices","MappingGetServices function [Internationalization for Windows Applications]","elscore/MappingGetServices","intl.mappinggetservices"]
old-location: intl\mappinggetservices.htm
tech.root: Intl
ms.assetid: 6d02e085-405e-4388-bf2f-409c92a7b190
ms.date: 12/05/2018
ms.keywords: MappingGetServices, MappingGetServices function [Internationalization for Windows Applications], elscore/MappingGetServices, intl.mappinggetservices
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
 - MappingGetServices
 - elscore/MappingGetServices
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
 - MappingGetServices
---

# MappingGetServices function


## -description

Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.

## -parameters

### -param pOptions [in, optional]

Pointer to a <a href="/windows/desktop/api/elscore/ns-elscore-mapping_enum_options">MAPPING_ENUM_OPTIONS</a> structure containing criteria to use during enumeration of services. The application specifies <b>NULL</b> for this parameter to retrieve all installed services.

### -param prgServices [out]

Address of a pointer to an array of <a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a> structures containing service information matching the criteria supplied in the <i>pOptions</i> parameter.

### -param pdwServicesCount [out]

Pointer to a DWORD variable in which this function retrieves the number of retrieved services.

## -returns

Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.<div class="alert"><b>Note</b>  The application must test for any failure before proceeding with further operations.</div>
<div> </div>

## -remarks

The ELS application can either retrieve all services or filter the services according to specified options. For an associated procedure and code sample, see <a href="/windows/desktop/Intl/enumerating-and-freeing-services">Enumerating and Freeing Services</a>.

To avoid resource leaks, the application must free the pointer indicated by <i>prgServices</i> with a call to <a href="/windows/desktop/api/elscore/nf-elscore-mappingfreeservices">MappingFreeServices</a>.  


For performance reasons, it is recommended to retrieve services infrequently. For example, if the application needs a specific service, by GUID, it can be enumerated when needed and cached for future use.

## -see-also

<a href="/windows/desktop/Intl/enumerating-and-freeing-services">Enumerating and Freeing Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services">Extended Linguistic Services</a>



<a href="/windows/desktop/Intl/extended-linguistic-services-functions">Extended Linguistic Services Functions</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_enum_options">MAPPING_ENUM_OPTIONS</a>



<a href="/windows/desktop/api/elscore/ns-elscore-mapping_service_info">MAPPING_SERVICE_INFO</a>



<a href="/windows/desktop/api/elscore/nf-elscore-mappingfreeservices">MappingFreeServices</a>