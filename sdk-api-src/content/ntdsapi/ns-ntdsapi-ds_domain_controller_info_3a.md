---
UID: NS:ntdsapi.DS_DOMAIN_CONTROLLER_INFO_3A
title: DS_DOMAIN_CONTROLLER_INFO_3A (ntdsapi.h)
description: The DS_DOMAIN_CONTROLLER_INFO_3 structure contains data about a domain controller. This structure is returned by the DsGetDomainControllerInfo function. (ANSI)
helpviewer_keywords: ["*PDS_DOMAIN_CONTROLLER_INFO_3A","DS_DOMAIN_CONTROLLER_INFO_3","DS_DOMAIN_CONTROLLER_INFO_3 structure [Active Directory]","DS_DOMAIN_CONTROLLER_INFO_3A","DS_DOMAIN_CONTROLLER_INFO_3W","PDS_DOMAIN_CONTROLLER_INFO_3","PDS_DOMAIN_CONTROLLER_INFO_3 structure pointer [Active Directory]","ad.ds_domain_controller_info_3","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3A","ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3W","ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_3"]
old-location: ad\ds_domain_controller_info_3.htm
tech.root: ad
ms.assetid: 510f458e-4c08-41c7-b290-1372ac9c8beb
ms.date: 12/05/2018
ms.keywords: '*PDS_DOMAIN_CONTROLLER_INFO_3A, DS_DOMAIN_CONTROLLER_INFO_3, DS_DOMAIN_CONTROLLER_INFO_3 structure [Active Directory], DS_DOMAIN_CONTROLLER_INFO_3A, DS_DOMAIN_CONTROLLER_INFO_3W, PDS_DOMAIN_CONTROLLER_INFO_3, PDS_DOMAIN_CONTROLLER_INFO_3 structure pointer [Active Directory], ad.ds_domain_controller_info_3, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3A, ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3W, ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_3'
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DS_DOMAIN_CONTROLLER_INFO_3W (Unicode) and DS_DOMAIN_CONTROLLER_INFO_3A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DS_DOMAIN_CONTROLLER_INFO_3A, *PDS_DOMAIN_CONTROLLER_INFO_3A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDS_DOMAIN_CONTROLLER_INFO_3A
 - ntdsapi/PDS_DOMAIN_CONTROLLER_INFO_3A
 - DS_DOMAIN_CONTROLLER_INFO_3A
 - ntdsapi/DS_DOMAIN_CONTROLLER_INFO_3A
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
 - DS_DOMAIN_CONTROLLER_INFO_3
 - DS_DOMAIN_CONTROLLER_INFO_3A
 - DS_DOMAIN_CONTROLLER_INFO_3W
---

# DS_DOMAIN_CONTROLLER_INFO_3A structure


## -description

The <b>DS_DOMAIN_CONTROLLER_INFO_3</b> structure contains data about a domain controller. This structure is returned by the 
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

### -field SiteObjectName

Pointer to a null-terminated  string that specifies the name of the site object on the domain controller.

### -field ComputerObjectName

Pointer to a null-terminated  string that specifies the name of the computer object on the domain controller.

### -field ServerObjectName

Pointer to a null-terminated  string that specifies the name of the server object on the domain controller.

### -field NtdsDsaObjectName

Pointer to a null-terminated  string that specifies the name of the NTDS DSA object on the domain controller.

### -field fIsPdc

A Boolean value that indicates whether or not this domain controller is the primary domain controller. If this value is <b>TRUE</b>, the domain controller is the primary domain controller; otherwise, the domain controller is not the primary domain controller.

### -field fDsEnabled

A Boolean value that indicates whether or not the domain controller is enabled. If this value is <b>TRUE</b>, the domain controller is enabled; otherwise, it is not enabled.

### -field fIsGc

A Boolean value that indicates whether or not the domain controller is global catalog server. If this value is <b>TRUE</b>, the domain controller is a global catalog server; otherwise, it is not a global catalog server.

### -field fIsRodc

A Boolean value that indicates if the domain controller is a read-only domain controller. If this value is <b>TRUE</b>, the domain controller is a read-only domain controller; otherwise, it is not a read-only domain controller.

### -field SiteObjectGuid

Contains the <b>GUID</b> for the site object on the domain controller.

### -field ComputerObjectGuid

Contains the <b>GUID</b> for the computer object on the domain controller.

### -field ServerObjectGuid

Contains the <b>GUID</b> for the server object on the domain controller.

### -field NtdsDsaObjectGuid

Contains the <b>GUID</b> for the NTDS DSA object on the domain controller.

## -remarks

The <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a> function can return different versions of this structure. For more information and a list of the currently supported versions, see the <i>InfoLevel</i> parameter of <b>DsGetDomainControllerInfo</b>.





> [!NOTE]
> The ntdsapi.h header defines DS_DOMAIN_CONTROLLER_INFO_3 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/AD/domain-controller-and-replication-management-structures">Domain Controller and Replication Management Structures</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa">DsGetDomainControllerInfo</a>

