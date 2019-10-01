---
UID: NF:ntdsapi.DsFreeDomainControllerInfoA
title: DsFreeDomainControllerInfoA function (ntdsapi.h)
author: windows-sdk-content
description: The DsFreeDomainControllerInfo function frees memory that is allocated by DsGetDomainControllerInfo for data about the domain controllers in a domain.
old-location: ad\dsfreedomaincontrollerinfo.htm
tech.root: ad
ms.assetid: 1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 1, 2, DsFreeDomainControllerInfo, DsFreeDomainControllerInfo function [Active Directory], DsFreeDomainControllerInfoA, DsFreeDomainControllerInfoW, _glines_dsfreedomaincontrollerinfo, ad.dsfreedomaincontrollerinfo, ntdsapi/DsFreeDomainControllerInfo, ntdsapi/DsFreeDomainControllerInfoA, ntdsapi/DsFreeDomainControllerInfoW
ms.topic: function
f1_keywords: 
 - "ntdsapi/DsFreeDomainControllerInfo"
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsFreeDomainControllerInfoW (Unicode) and DsFreeDomainControllerInfoA (ANSI)
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
 - DsFreeDomainControllerInfo
 - DsFreeDomainControllerInfoA
 - DsFreeDomainControllerInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DsFreeDomainControllerInfoA function


## -description


The <b>DsFreeDomainControllerInfo</b> function frees memory that is allocated by 
<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> for data about the domain controllers in a domain.


## -parameters




### -param InfoLevel [in]

Indicates what version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure should be freed. This parameter can be one of the following values.



#### 1

The function frees the structure that contains  <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a> data.



#### 2

The function frees the structure that contains <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a> data.


### -param cInfo [in]

Indicates the number of items in <i>pInfo</i>.


### -param pInfo [in]

Pointer to an array of <a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO</a> structures to be freed.


## -returns



This function does not return a value.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a>
 

 

