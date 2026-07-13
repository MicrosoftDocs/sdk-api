---
UID: NF:ntdsapi.DsFreeDomainControllerInfoW
title: DsFreeDomainControllerInfoW function (ntdsapi.h)
description: The DsFreeDomainControllerInfo function frees memory that is allocated by DsGetDomainControllerInfo for data about the domain controllers in a domain. (Unicode)
helpviewer_keywords: ["1", "2", "DsFreeDomainControllerInfo", "DsFreeDomainControllerInfo function [Active Directory]", "DsFreeDomainControllerInfoW", "_glines_dsfreedomaincontrollerinfo", "ad.dsfreedomaincontrollerinfo", "ntdsapi/DsFreeDomainControllerInfo", "ntdsapi/DsFreeDomainControllerInfoW"]
old-location: ad\dsfreedomaincontrollerinfo.htm
tech.root: ad
ms.assetid: 1b6d3136-91e2-4653-a4b0-ae2f66a6c5a2
ms.date: 12/05/2018
ms.keywords: 1, 2, DsFreeDomainControllerInfo, DsFreeDomainControllerInfo function [Active Directory], DsFreeDomainControllerInfoA, DsFreeDomainControllerInfoW, _glines_dsfreedomaincontrollerinfo, ad.dsfreedomaincontrollerinfo, ntdsapi/DsFreeDomainControllerInfo, ntdsapi/DsFreeDomainControllerInfoA, ntdsapi/DsFreeDomainControllerInfoW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsFreeDomainControllerInfoW
 - ntdsapi/DsFreeDomainControllerInfoW
dev_langs:
 - c++
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
---

# DsFreeDomainControllerInfoW function


## -description

The <b>DsFreeDomainControllerInfo</b> function frees memory that is allocated by 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> for data about the domain controllers in a domain.

## -parameters

### -param InfoLevel [in]

Indicates what version of the <b>DS_DOMAIN_CONTROLLER_INFO</b> structure should be freed. This parameter can be one of the following values.



#### 1

The function frees the structure that contains  <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a> data.



#### 2

The function frees the structure that contains <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a> data.

### -param cInfo [in]

Indicates the number of items in <i>pInfo</i>.

### -param pInfo [in]

Pointer to an array of <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO</a> structures to be freed.


##### - InfoLevel.1

The function frees the structure that contains  <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a> data.


##### - InfoLevel.2

The function frees the structure that contains <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a">DS_DOMAIN_CONTROLLER_INFO_2</a> data.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a">DS_DOMAIN_CONTROLLER_INFO_1</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a>

## -remarks

> [!NOTE]
> The ntdsapi.h header defines DsFreeDomainControllerInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
