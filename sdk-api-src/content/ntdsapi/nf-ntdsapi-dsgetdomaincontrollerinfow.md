---
UID: NF:ntdsapi.DsGetDomainControllerInfoW
title: DsGetDomainControllerInfoW function
author: windows-sdk-content
description: Retrieves data about the domain controllers in a domain.
old-location: ad\dsgetdomaincontrollerinfo.htm
old-project: AD
ms.assetid: 52db3b25-e6b0-4a0d-831b-89a203580cf1
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: 1, 2, 3, DsGetDomainControllerInfo, DsGetDomainControllerInfo function [Active Directory], DsGetDomainControllerInfoA, DsGetDomainControllerInfoW, _glines_dsgetdomaincontrollerinfo, ad.dsgetdomaincontrollerinfo, ntdsapi/DsGetDomainControllerInfo, ntdsapi/DsGetDomainControllerInfoA, ntdsapi/DsGetDomainControllerInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDomainControllerInfoW (Unicode) and DsGetDomainControllerInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DS_REPL_OP_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
 - API-MS-Win-Security-ActiveDirectoryClient-l1-1-0.dll
 - KernelBase.dll
 - API-Ms-Win-Security-ActiveDirectoryClient-L1-1-1.dll
api_name:
 - DsGetDomainControllerInfo
 - DsGetDomainControllerInfoA
 - DsGetDomainControllerInfoW
product: Windows
targetos: Windows
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
req.product: ADAM
---

# DsGetDomainControllerInfoW function


## -description


The <b>DsGetDomainControllerInfo</b> function retrieves data about the domain controllers in a domain.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DSBind</a> or 
<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DSBindWithCred</a> function.


### -param DomainName [in]

Pointer to a null-terminated string that specifies the domain name.


### -param InfoLevel [in]

Contains a value that indicates the version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure to  return. This can be one of the following values.



#### 1

The function provides the domain data in the <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a> structure format.



#### 2

The function provides the domain data in the <a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a> structure format.



#### 3

The function provides the domain data in the <a href="https://msdn.microsoft.com/510f458e-4c08-41c7-b290-1372ac9c8beb">DS_DOMAIN_CONTROLLER_INFO_3</a> structure format.


### -param pcOut [out]

Pointer to a <b>DWORD</b> variable that receives the number of items returned in <i>ppInfo</i> array.


### -param ppInfo [out]

Pointer to a pointer variable that receives an array of  <b>DS_DOMAIN_CONTROLLER_INFO_*</b> structures. The type of structures in this array is defined by the <i>InfoLevel</i> parameter. The caller must free this array, when it is no longer required, by using 
the <a href="https://msdn.microsoft.com/1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2">DsFreeDomainControllerInfo</a> function.


##### - InfoLevel.1

The function provides the domain data in the <a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a> structure format.


##### - InfoLevel.2

The function provides the domain data in the <a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a> structure format.


##### - InfoLevel.3

The function provides the domain data in the <a href="https://msdn.microsoft.com/510f458e-4c08-41c7-b290-1372ac9c8beb">DS_DOMAIN_CONTROLLER_INFO_3</a> structure format.


## -returns



If the function returns domain controller data, the return value is <b>ERROR_SUCCESS</b>. If the caller does not have the privileges to access the server objects, the return value is <b>ERROR_SUCCESS</b>, but the <b>DS_DOMAIN_CONTROLLER_INFO</b> structures could be empty.

If the function fails, the return value can be one of the following error codes.




## -see-also




<a href="https://msdn.microsoft.com/6cc829ac-2aa6-49ef-b1ab-9c249249e0d6">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://msdn.microsoft.com/9d45b732-363d-4b20-ae5c-e9e76264bf1f">DS_DOMAIN_CONTROLLER_INFO_2</a>



<a href="https://msdn.microsoft.com/510f458e-4c08-41c7-b290-1372ac9c8beb">DS_DOMAIN_CONTROLLER_INFO_3</a>



<a href="https://msdn.microsoft.com/a92783c2-ffb8-473e-8484-1c05ca5453ff">Domain Controller and Replication Management Functions</a>



<a href="https://msdn.microsoft.com/c73cd16d-ccfd-4f61-b1c5-50130bef64d7">DsBind</a>



<a href="https://msdn.microsoft.com/708e3874-852c-4a57-bf4b-edaf98818fe5">DsBindWithCred</a>



<a href="https://msdn.microsoft.com/1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2">DsFreeDomainControllerInfo</a>
 

 

