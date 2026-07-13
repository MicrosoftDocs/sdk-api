---
UID: NF:dsgetdc.DsGetDcOpenA
title: DsGetDcOpenA function (dsgetdc.h)
description: Opens a new domain controller enumeration operation. (ANSI)
helpviewer_keywords: ["DS_FORCE_REDISCOVERY", "DS_GC_SERVER_REQUIRED", "DS_KDC_REQUIRED", "DS_NOTIFY_AFTER_SITE_RECORDS", "DS_ONLY_DO_SITE_NAME", "DS_ONLY_LDAP_NEEDED", "DS_PDC_REQUIRED", "DsGetDcOpenA", "dsgetdc/DsGetDcOpenA"]
old-location: ad\dsgetdcopen.htm
tech.root: ad
ms.assetid: 2811cc30-f367-4f1a-8f0c-ed0a77dad24c
ms.date: 12/05/2018
ms.keywords: DS_FORCE_REDISCOVERY, DS_GC_SERVER_REQUIRED, DS_KDC_REQUIRED, DS_NOTIFY_AFTER_SITE_RECORDS, DS_ONLY_DO_SITE_NAME, DS_ONLY_LDAP_NEEDED, DS_PDC_REQUIRED, DsGetDcOpen, DsGetDcOpen function [Active Directory], DsGetDcOpenA, DsGetDcOpenW, ad.dsgetdcopen, dsgetdc/DsGetDcOpen, dsgetdc/DsGetDcOpenA, dsgetdc/DsGetDcOpenW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsGetDcOpenW (Unicode) and DsGetDcOpenA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DsGetDcOpenA
 - dsgetdc/DsGetDcOpenA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - DsGetDcOpen
 - DsGetDcOpenA
 - DsGetDcOpenW
---

# DsGetDcOpenA function


## -description

The <b>DsGetDcOpen</b> function opens a new domain controller enumeration operation.

## -parameters

### -param DnsName [in]

Pointer to a null-terminated string that contains the domain naming system (DNS) name of the domain to enumerate the domain controllers for. This parameter cannot be <b>NULL</b>.

### -param OptionFlags [in]

Contains a set of flags that modify the behavior of the function. This can be zero or a combination of one or more of the following values.



#### DS_ONLY_DO_SITE_NAME

Only site-specific domain controllers are enumerated.



#### DS_NOTIFY_AFTER_SITE_RECORDS

The <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnexta">DsGetDcNext</a> function will return the <b>ERROR_FILEMARK_DETECTED</b> value after all of the site-specific domain controllers are retrieved. <b>DsGetDcNext</b> will then enumerate the second group, which contains all domain controllers in the domain, including the site-specific domain controllers contained in the first group.

### -param SiteName [in, optional]

Pointer to a null-terminated string that contains the name of site the client is in. This parameter is optional and may be <b>NULL</b>.

### -param DomainGuid [in, optional]

Pointer to a <b>GUID</b> value that contains the identifier of the domain specified by <i>DnsName</i>.
        This identifier is used to handle the case of a renamed domain.  If this
        value is specified and the domain specified in <i>DnsName</i> is renamed, this function attempts to enumerate domain controllers in the domain that contains the specified identifier. This parameter is optional and may be <b>NULL</b>.

### -param DnsForestName [in, optional]

Pointer to a null-terminated string that contains the name of the forest that contains the <i>DnsName</i> domain.  This value is used in conjunction with <i>DomainGuid</i> to enumerate the domain controllers if the  domain has been renamed. This parameter is optional and may be <b>NULL</b>.

### -param DcFlags [in]

Contains a set of flags that identify the type of domain controllers to enumerate. This can be zero or a combination of one or more of the following values.



#### DS_FORCE_REDISCOVERY

Forces cached domain controller data to be ignored. When this flag is not specified, <b>DsGetDcOpen</b> obtains the domain controller enumeration from cached domain controller data.



#### DS_GC_SERVER_REQUIRED

Requires that the enumerated domain controllers be global catalog servers for the forest of domains with this domain as the root. This flag cannot be combined with the <b>DS_PDC_REQUIRED</b> flag.



#### DS_KDC_REQUIRED

Requires that the enumerated domain controllers currently be  running the Kerberos Key Distribution Center service. This flag cannot be combined with the <b>DS_PDC_REQUIRED</b> or <b>DS_GC_SERVER_REQUIRED</b> flags.



#### DS_ONLY_LDAP_NEEDED

Specifies that the enumerated servers are LDAP servers. The servers are not necessarily domain controllers. No other services are implied to be present at each enumerated server. The servers do not necessarily have a writable <b>config</b> container nor a writable <b>schema</b> container. The servers may not necessarily be used to create or modify security principles. This flag may be used with the <b>DS_GC_SERVER_REQUIRED</b> flag to enumerate LDAP servers that also host a global catalog server. In that case, the enumerated global catalog servers are not necessarily  domain controllers and other services are implied to be present at each server. If this flag is specified, the <b>DS_PDC_REQUIRED</b>, <b>DS_TIMESERV_REQUIRED</b>, <b>DS_GOOD_TIMESERV_PREFERRED</b>, <b>DS_DIRECTORY_SERVICES_PREFERED</b>, <b>DS_DIRECTORY_SERVICES_REQUIRED</b>, and <b>DS_KDC_REQUIRED</b> flags are ignored.



#### DS_PDC_REQUIRED

Requires that the enumerated domain controllers be the primary domain controllers for the domain. This flag cannot be combined with the <b>DS_GC_SERVER_REQUIRED</b> flag.

### -param RetGetDcContext [out]

Pointer to a <b>HANDLE</b> value that receives the domain controller enumeration context handle. This handle is used with the <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnexta">DsGetDcNext</a> function to identify the domain controller enumeration operation. This handle is passed to <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcclosew">DsGetDcClose</a> to close the domain controller enumeration operation.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 or RPC error otherwise. Possible error values include the following.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcclosew">DsGetDcClose</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcnexta">DsGetDcNext</a>



<a href="/windows/desktop/AD/enumerating-domain-controllers">Enumerating Domain Controllers</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DsGetDcOpen as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
