---
UID: NF:ntdsapi.DsGetDomainControllerInfoW
title: DsGetDomainControllerInfoW function (ntdsapi.h)
description: Retrieves data about the domain controllers in a domain.helpviewer_keywords: ["1","2","3","DsGetDomainControllerInfo","DsGetDomainControllerInfo function [Active Directory]","DsGetDomainControllerInfoA","DsGetDomainControllerInfoW","_glines_dsgetdomaincontrollerinfo","ad.dsgetdomaincontrollerinfo","ntdsapi/DsGetDomainControllerInfo","ntdsapi/DsGetDomainControllerInfoA","ntdsapi/DsGetDomainControllerInfoW"]
old-location: ad\dsgetdomaincontrollerinfo.htm
tech.root: ad
ms.assetid: 52db3b25-e6b0-4a0d-831b-89a203580cf1
ms.date: 12/05/2018
ms.keywords: 1, 2, 3, DsGetDomainControllerInfo, DsGetDomainControllerInfo function [Active Directory], DsGetDomainControllerInfoA, DsGetDomainControllerInfoW, _glines_dsgetdomaincontrollerinfo, ad.dsgetdomaincontrollerinfo, ntdsapi/DsGetDomainControllerInfo, ntdsapi/DsGetDomainControllerInfoA, ntdsapi/DsGetDomainControllerInfoW
f1_keywords:
- ntdsapi/DsGetDomainControllerInfo
dev_langs:
- c++
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
req.lib: Ntdsapi.lib
req.dll: Ntdsapi.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsGetDomainControllerInfoW function


## -description


The <b>DsGetDomainControllerInfo</b> function retrieves data about the domain controllers in a domain.


## -parameters




### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.


### -param DomainName [in]

Pointer to a null-terminated string that specifies the domain name.


### -param InfoLevel [in]

Contains a value that indicates the version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure to  return. This can be one of the following values.



#### 1

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a> structure format.



#### 2

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a> structure format.



#### 3

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a">DS_DOMAIN_CONTROLLER_INFO_3</a> structure format.


### -param pcOut [out]

Pointer to a <b>DWORD</b> variable that receives the number of items returned in <i>ppInfo</i> array.


### -param ppInfo [out]

Pointer to a pointer variable that receives an array of  <b>DS_DOMAIN_CONTROLLER_INFO_*</b> structures. The type of structures in this array is defined by the <i>InfoLevel</i> parameter. The caller must free this array, when it is no longer required, by using 
the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa">DsFreeDomainControllerInfo</a> function.


##### - InfoLevel.1

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a> structure format.


##### - InfoLevel.2

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a> structure format.


##### - InfoLevel.3

The function provides the domain data in the <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a">DS_DOMAIN_CONTROLLER_INFO_3</a> structure format.


## -returns



If the function returns domain controller data, the return value is <b>ERROR_SUCCESS</b>. If the caller does not have the privileges to access the server objects, the return value is <b>ERROR_SUCCESS</b>, but the <b>DS_DOMAIN_CONTROLLER_INFO</b> structures could be empty.

If the function fails, the return value can be one of the following error codes.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a">DS_DOMAIN_CONTROLLER_INFO_3</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DsBind</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DsBindWithCred</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa">DsFreeDomainControllerInfo</a>
 

 

