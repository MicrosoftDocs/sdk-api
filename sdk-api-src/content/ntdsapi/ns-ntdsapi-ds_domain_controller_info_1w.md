---
UID: NS:ntdsapi.DS_DOMAIN_CONTROLLER_INFO_1W
title: DS_DOMAIN_CONTROLLER_INFO_1W (ntdsapi.h)
description: The DS_DOMAIN_CONTROLLER_INFO_1 structure contains data about a domain controller. This structure is returned by the DsGetDomainControllerInfo function. (Unicode)
helpviewer_keywords: ["*PDS_DOMAIN_CONTROLLER_INFO_1W","DS_DOMAIN_CONTROLLER_INFO_1","DS_DOMAIN_CONTROLLER_INFO_1 structure [Active Directory]","DS_DOMAIN_CONTROLLER_INFO_1A","DS_DOMAIN_CONTROLLER_INFO_1W","PDS_DOMAIN_CONTROLLER_INFO_1","PDS_DOMAIN_CONTROLLER_INFO_1 structure pointer [Active Directory]","_glines_ds_domain_controller_info_1","ad.ds__domain__controller__info__1","ad.ds_domain_controller_info_1","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1A","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1W","ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_1"]
old-location: ad\ds_domain_controller_info_1.htm
tech.root: ad
ms.assetid: 6cc829ac-2aa6-49ef-b1ab-9c249249e0d6
ms.date: 12/05/2018
ms.keywords: '*PDS_DOMAIN_CONTROLLER_INFO_1W, DS_DOMAIN_CONTROLLER_INFO_1, DS_DOMAIN_CONTROLLER_INFO_1 structure [Active Directory], DS_DOMAIN_CONTROLLER_INFO_1A, DS_DOMAIN_CONTROLLER_INFO_1W, PDS_DOMAIN_CONTROLLER_INFO_1, PDS_DOMAIN_CONTROLLER_INFO_1 structure pointer [Active Directory], _glines_ds_domain_controller_info_1, ad.ds__domain__controller__info__1, ad.ds_domain_controller_info_1, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1A, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1W, ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_1'
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_DOMAIN_CONTROLLER_INFO_1W (Unicode) and DS_DOMAIN_CONTROLLER_INFO_1A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DS_DOMAIN_CONTROLLER_INFO_1W, *PDS_DOMAIN_CONTROLLER_INFO_1W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDS_DOMAIN_CONTROLLER_INFO_1W
 - ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_1W
 - DS_DOMAIN_CONTROLLER_INFO_1W
 - ntdsapi/DS_DOMAIN_CONTROLLER_INFO_1W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_DOMAIN_CONTROLLER_INFO_1
 - DS_DOMAIN_CONTROLLER_INFO_1A
 - DS_DOMAIN_CONTROLLER_INFO_1W
---

# DS_DOMAIN_CONTROLLER_INFO_1W structure


## -description

The <b>DS_DOMAIN_CONTROLLER_INFO_1</b> structure contains data about a domain controller. This structure is returned by the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> function.

## -struct-fields

### -field string

### -field unique

### -field NetbiosName

Pointer to a null-terminated string that specifies the NetBIOS name of the domain controller.

### -field DnsHostName

Pointer to a null-terminated  string that specifies the DNS host name of the domain controller.

### -field SiteName

Pointer to a null-terminated  string that specifies the site to which the domain controller belongs.

### -field ComputerObjectName

Pointer to a null-terminated  string that specifies the name of the computer object on the domain controller.

### -field ServerObjectName

Pointer to a null-terminated  string that specifies the name of the server object on the domain controller.

### -field fIsPdc

A Boolean value that indicates whether or not this domain controller is the primary domain controller. If this value is <b>TRUE</b>, the domain controller is the primary domain controller; otherwise, the domain controller is not the primary domain controller.

### -field fDsEnabled

A Boolean value that indicates whether or not the domain controller is enabled. If this value is <b>TRUE</b>, the domain controller is enabled; otherwise, it is not enabled.

## -remarks

The <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> function can return different versions of this structure. For more information and a list of the currently supported versions, see the <i>InfoLevel</i> parameter of <b>DsGetDomainControllerInfo</b>.





> [!NOTE]
> The ntdsapi.h header defines DS_DOMAIN_CONTROLLER_INFO_1 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a>

