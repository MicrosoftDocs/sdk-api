---
UID: NF:elscore.MappingGetServices
title: MappingGetServices function
author: windows-sdk-content
description: Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.
old-location: intl\mappinggetservices.htm
old-project: Intl
ms.assetid: 6d02e085-405e-4388-bf2f-409c92a7b190
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: MappingGetServices, MappingGetServices function [Internationalization for Windows Applications], elscore/MappingGetServices, intl.mappinggetservices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: ENHANCED_STORAGE_PASSWORD_SILO_INFORMATION, *PENHANCED_STORAGE_PASSWORD_SILO_INFORMATION
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
product: Windows
targetos: Windows
req.lib: Elscore.lib
req.dll: Elscore.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# MappingGetServices function


## -description


Retrieves a list of available ELS platform-supported services, along with associated information, according to application-specified criteria.


## -parameters




### -param pOptions [in, optional]

Pointer to a <a href="https://msdn.microsoft.com/3c5a0c04-9789-48dc-bc8f-a8b5ff350e27">MAPPING_ENUM_OPTIONS</a> structure containing criteria to use during enumeration of services. The application specifies <b>NULL</b> for this parameter to retrieve all installed services.


### -param prgServices [out]

Address of a pointer to an array of <a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a> structures containing service information matching the criteria supplied in the <i>pOptions</i> parameter.


### -param pdwServicesCount [out]

Pointer to a DWORD variable in which this function retrieves the number of retrieved services. 


## -returns



Returns S_OK if successful. The function returns an error HRESULT value if it does not succeed.<div class="alert"><b>Note</b>  The application must test for any failure before proceeding with further operations.</div>
<div> </div>





## -remarks



The ELS application can either retrieve all services or filter the services according to specified options. For an associated procedure and code sample, see <a href="https://msdn.microsoft.com/526e51c7-9ff2-4590-b092-172f4942ce8e">Enumerating and Freeing Services</a>.

To avoid resource leaks, the application must free the pointer indicated by <i>prgServices</i> with a call to <a href="https://msdn.microsoft.com/3b90c1c5-3007-4c5d-a51b-e77b1f9c2dd0">MappingFreeServices</a>.  


For performance reasons, it is recommended to retrieve services infrequently. For example, if the application needs a specific service, by GUID, it can be enumerated when needed and cached for future use.




## -see-also




<a href="https://msdn.microsoft.com/526e51c7-9ff2-4590-b092-172f4942ce8e">Enumerating and Freeing Services</a>



<a href="https://msdn.microsoft.com/90bc1757-ec94-425e-927f-9ae2e1ab8af8">Extended Linguistic Services</a>



<a href="https://msdn.microsoft.com/d62ab664-a75a-4d06-aefb-a3311ea7d4a7">Extended Linguistic Services Functions</a>



<a href="https://msdn.microsoft.com/3c5a0c04-9789-48dc-bc8f-a8b5ff350e27">MAPPING_ENUM_OPTIONS</a>



<a href="https://msdn.microsoft.com/444102a7-0da9-44be-989e-7a5139320034">MAPPING_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/3b90c1c5-3007-4c5d-a51b-e77b1f9c2dd0">MappingFreeServices</a>
 

 

