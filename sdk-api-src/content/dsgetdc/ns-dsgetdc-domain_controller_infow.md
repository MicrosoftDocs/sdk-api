---
UID: NS:dsgetdc._DOMAIN_CONTROLLER_INFOW
title: DOMAIN_CONTROLLER_INFOW (dsgetdc.h)
description: Used with the DsGetDcName function to receive data about a domain controller. (Unicode)
helpviewer_keywords: ["*PDOMAIN_CONTROLLER_INFOW","DOMAIN_CONTROLLER_INFO","DOMAIN_CONTROLLER_INFO structure [Active Directory]","DOMAIN_CONTROLLER_INFOA","DOMAIN_CONTROLLER_INFOW","DS_CLOSEST_FLAG","DS_DNS_CONTROLLER_FLAG","DS_DNS_DOMAIN_FLAG","DS_DNS_FOREST_FLAG","DS_DS_FLAG","DS_FULL_SECRET_DOMAIN_6_FLAG","DS_GC_FLAG","DS_GOOD_TIMESERV_FLAG","DS_INET_ADDRESS","DS_KDC_FLAG","DS_LDAP_FLAG","DS_NDNC_FLAG","DS_NETBIOS_ADDRESS","DS_PDC_FLAG","DS_SELECT_SECRET_DOMAIN_6_FLAG","DS_TIMESERV_FLAG","DS_WRITABLE_FLAG","PDOMAIN_CONTROLLER_INFO","PDOMAIN_CONTROLLER_INFO structure pointer [Active Directory]","_glines_domain_controller_info","ad.domain__controller__info","ad.domain_controller_info","dsgetdc/DOMAIN_CONTROLLER_INFO","dsgetdc/DOMAIN_CONTROLLER_INFOA","dsgetdc/DOMAIN_CONTROLLER_INFOW","dsgetdc/PDOMAIN_CONTROLLER_INFO"]
old-location: ad\domain_controller_info.htm
tech.root: ad
ms.assetid: 0c09fe26-ef53-48b1-8ac2-70ccb8f3e3e2
ms.date: 12/05/2018
ms.keywords: '*PDOMAIN_CONTROLLER_INFOW, DOMAIN_CONTROLLER_INFO, DOMAIN_CONTROLLER_INFO structure [Active Directory], DOMAIN_CONTROLLER_INFOA, DOMAIN_CONTROLLER_INFOW, DS_CLOSEST_FLAG, DS_DNS_CONTROLLER_FLAG, DS_DNS_DOMAIN_FLAG, DS_DNS_FOREST_FLAG, DS_DS_FLAG, DS_FULL_SECRET_DOMAIN_6_FLAG, DS_GC_FLAG, DS_GOOD_TIMESERV_FLAG, DS_INET_ADDRESS, DS_KDC_FLAG, DS_LDAP_FLAG, DS_NDNC_FLAG, DS_NETBIOS_ADDRESS, DS_PDC_FLAG, DS_SELECT_SECRET_DOMAIN_6_FLAG, DS_TIMESERV_FLAG, DS_WRITABLE_FLAG, PDOMAIN_CONTROLLER_INFO, PDOMAIN_CONTROLLER_INFO structure pointer [Active Directory], _glines_domain_controller_info, ad.domain__controller__info, ad.domain_controller_info, dsgetdc/DOMAIN_CONTROLLER_INFO, dsgetdc/DOMAIN_CONTROLLER_INFOA, dsgetdc/DOMAIN_CONTROLLER_INFOW, dsgetdc/PDOMAIN_CONTROLLER_INFO'
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DOMAIN_CONTROLLER_INFOW (Unicode) and DOMAIN_CONTROLLER_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DOMAIN_CONTROLLER_INFOW, *PDOMAIN_CONTROLLER_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOMAIN_CONTROLLER_INFOW
 - dsgetdc/_DOMAIN_CONTROLLER_INFOW
 - PDOMAIN_CONTROLLER_INFOW
 - dsgetdc/PDOMAIN_CONTROLLER_INFOW
 - DOMAIN_CONTROLLER_INFOW
 - dsgetdc/DOMAIN_CONTROLLER_INFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsgetdc.h
api_name:
 - DOMAIN_CONTROLLER_INFO
 - DOMAIN_CONTROLLER_INFOA
 - DOMAIN_CONTROLLER_INFOW
---

# DOMAIN_CONTROLLER_INFOW structure


## -description

The <b>DOMAIN_CONTROLLER_INFO</b> structure is used with the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a> function to receive  data about a domain controller.

## -struct-fields

### -field DomainControllerName.string

### -field DomainControllerName.unique

### -field DomainControllerName

Pointer to a null-terminated string that specifies the computer name of the discovered domain controller. The returned computer name is prefixed with "\\". The DNS-style name, for example, "\\phoenix.fabrikam.com", is returned, if available. If the DNS-style name is not available, the flat-style name (for example, "\\phoenix") is returned. This example would apply if the domain is a Windows NT 4.0 domain or if the domain does not support the IP family of protocols.

### -field DomainControllerAddress.string

### -field DomainControllerAddress.unique

### -field DomainControllerAddress

Pointer to a null-terminated string that specifies the address of the discovered domain controller. The address is prefixed with "\\". This string is one of the types defined by the <b>DomainControllerAddressType</b> member.

### -field DomainControllerAddressType

Indicates the type of string that is contained in the <b>DomainControllerAddress</b> member. This can be one of the following values.



#### DS_INET_ADDRESS

The address is a string IP address (for example, "\\157.55.94.74") of the domain controller.



#### DS_NETBIOS_ADDRESS

The address is a NetBIOS name, for example, "\\phoenix", of the domain controller.

### -field DomainGuid

The <b>GUID</b> of the domain. This member is zero if the domain controller does not have a Domain GUID; for example, the domain controller is not a Windows 2000 domain controller.

### -field DomainName.string

### -field DomainName.unique

### -field DomainName

Pointer to a null-terminated string that specifies the name of the domain. The DNS-style name, for example, "fabrikam.com", is returned if available. Otherwise, the flat-style name, for example, "fabrikam", is returned. This name may be different than the requested domain name if the domain has been renamed.

### -field DnsForestName.string

### -field DnsForestName.unique

### -field DnsForestName

Pointer to a null-terminated string that specifies the name of the domain at the root of the DS tree. The DNS-style name, for example, "fabrikam.com", is returned if available. Otherwise, the flat-style name, for example, "fabrikam" is returned.

### -field Flags

Contains a set of flags that describe the domain controller. 
This can be zero or a combination of one or more of the following values.



#### DS_DNS_CONTROLLER_FLAG

The <b>DomainControllerName</b> member is in DNS format.



#### DS_DNS_DOMAIN_FLAG

The <b>DomainName</b> member is in DNS format.



#### DS_DNS_FOREST_FLAG

The <b>DnsForestName</b> member is in DNS format.



#### DS_CLOSEST_FLAG

The domain controller is in the same site as the client.



#### DS_DS_FLAG

The domain controller is a directory service server for the domain.



#### DS_FULL_SECRET_DOMAIN_6_FLAG

The domain controller is a Windows 2008 or later writable domain controller.



#### DS_GOOD_TIMESERV_FLAG

The domain controller is running a reliable Windows Time Service for the domain.



#### DS_GC_FLAG

The domain controller is a global catalog server for the forest specified by <b>DnsForestName</b>.



#### DS_KDC_FLAG

The domain controller is a Kerberos Key Distribution Center for the domain.



#### DS_LDAP_FLAG

The server is an LDAP server.



#### DS_NDNC_FLAG

The Domain Name is an application (non-domain) naming context.



#### DS_PDC_FLAG

The domain controller is the primary domain controller of the domain.



#### DS_SELECT_SECRET_DOMAIN_6_FLAG

The domain controller is a Windows 2008 or later read-only domain controller.



#### DS_TIMESERV_FLAG

The domain controller is running the Windows Time Service for the domain.



#### DS_WRITABLE_FLAG

The domain controller hosts a writable directory service (or SAM).

### -field DcSiteName.string

### -field DcSiteName.unique

### -field DcSiteName

Pointer to a null-terminated string that specifies the name of the site where the domain controller is located. This member may be <b>NULL</b> if the domain controller is not in a site; for example, the domain controller is a Windows NT 4.0 domain controller.

### -field ClientSiteName.string

### -field ClientSiteName.unique

### -field ClientSiteName

Pointer to a null-terminated string that specifies the name of the site that the computer belongs to. The computer is specified in the <i>ComputerName</i> parameter passed to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>. This member may be <b>NULL</b> if the site that contains the computer cannot be found; for example, if the DS administrator has not associated the subnet that the computer is in with a valid site.


##### - DomainControllerAddressType.DS_INET_ADDRESS

The address is a string IP address (for example, "\\157.55.94.74") of the domain controller.


##### - DomainControllerAddressType.DS_NETBIOS_ADDRESS

The address is a NetBIOS name, for example, "\\phoenix", of the domain controller.


##### - Flags.DS_CLOSEST_FLAG

The domain controller is in the same site as the client.


##### - Flags.DS_DNS_CONTROLLER_FLAG

The <b>DomainControllerName</b> member is in DNS format.


##### - Flags.DS_DNS_DOMAIN_FLAG

The <b>DomainName</b> member is in DNS format.


##### - Flags.DS_DNS_FOREST_FLAG

The <b>DnsForestName</b> member is in DNS format.


##### - Flags.DS_DS_FLAG

The domain controller is a directory service server for the domain.


##### - Flags.DS_FULL_SECRET_DOMAIN_6_FLAG

The domain controller is a Windows 2008 or later writable domain controller.


##### - Flags.DS_GC_FLAG

The domain controller is a global catalog server for the forest specified by <b>DnsForestName</b>.


##### - Flags.DS_GOOD_TIMESERV_FLAG

The domain controller is running a reliable Windows Time Service for the domain.


##### - Flags.DS_KDC_FLAG

The domain controller is a Kerberos Key Distribution Center for the domain.


##### - Flags.DS_LDAP_FLAG

The server is an LDAP server.


##### - Flags.DS_NDNC_FLAG

The Domain Name is an application (non-domain) naming context.


##### - Flags.DS_PDC_FLAG

The domain controller is the primary domain controller of the domain.


##### - Flags.DS_SELECT_SECRET_DOMAIN_6_FLAG

The domain controller is a Windows 2008 or later read-only domain controller.


##### - Flags.DS_TIMESERV_FLAG

The domain controller is running the Windows Time Service for the domain.


##### - Flags.DS_WRITABLE_FLAG

The domain controller hosts a writable directory service (or SAM).

## -see-also

<a href="/windows/desktop/AD/directory-service-structures">Directory Service Structures</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnamea">DsGetDcName</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DOMAIN_CONTROLLER_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
