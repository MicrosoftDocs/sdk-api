---
UID: NF:dsgetdc.DsDeregisterDnsHostRecordsW
title: DsDeregisterDnsHostRecordsW function (dsgetdc.h)
description: The DsDeregisterDnsHostRecords function deletes DNS entries, except for type A records registered by a domain controller. Only an administrator, account operator, or server operator may call this function. (Unicode)
helpviewer_keywords: ["DsDeregisterDnsHostRecords", "DsDeregisterDnsHostRecords function [Active Directory]", "DsDeregisterDnsHostRecordsW", "_glines_dsderegisterdnshostrecords", "ad.dsderegisterdnshostrecords", "dsgetdc/DsDeregisterDnsHostRecords", "dsgetdc/DsDeregisterDnsHostRecordsW"]
old-location: ad\dsderegisterdnshostrecords.htm
tech.root: ad
ms.assetid: 18ab6455-dab2-42d9-b68e-a8f0ad2d8091
ms.date: 12/05/2018
ms.keywords: DsDeregisterDnsHostRecords, DsDeregisterDnsHostRecords function [Active Directory], DsDeregisterDnsHostRecordsA, DsDeregisterDnsHostRecordsW, _glines_dsderegisterdnshostrecords, ad.dsderegisterdnshostrecords, dsgetdc/DsDeregisterDnsHostRecords, dsgetdc/DsDeregisterDnsHostRecordsA, dsgetdc/DsDeregisterDnsHostRecordsW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsDeregisterDnsHostRecordsW (Unicode) and DsDeregisterDnsHostRecordsA (ANSI)
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
 - DsDeregisterDnsHostRecordsW
 - dsgetdc/DsDeregisterDnsHostRecordsW
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
 - DsDeregisterDnsHostRecords
 - DsDeregisterDnsHostRecordsA
 - DsDeregisterDnsHostRecordsW
---

# DsDeregisterDnsHostRecordsW function


## -description

The <b>DsDeregisterDnsHostRecords</b> function deletes DNS entries, except for type A records registered by a domain controller. Only an administrator, account operator, or server operator may call this function.

## -parameters

### -param ServerName [in, optional]

The null-terminated string that specifies the name of the remote domain controller. Can be set to <b>NULL</b> if the calling application is running on the domain controller being updated.

### -param DnsDomainName [in, optional]

The null-terminated string that specifies the DNS domain name of the domain occupied by the domain controller. It is unnecessary for this to be a domain hosted by this domain controller. If <b>NULL</b>, the <i>DnsHostName</i> with the leftmost label removed is specified.

### -param DomainGuid [in, optional]

Pointer to the Domain GUID of the domain. If <b>NULL</b>, GUID specific names are not removed.

### -param DsaGuid [in, optional]

Pointer to the GUID of the <b>NTDS-DSA</b> object to be deleted. If <b>NULL</b>, <b>NTDS-DSA</b> specific names are not removed.

### -param DnsHostName [in]

Pointer to the null-terminated string that specifies the DNS host name of the domain controller whose DNS records are being deleted.

## -returns

This function returns DSGETDCAPI DWORD.

## -remarks

This function deregisters SRV and CNAME records only. It leaves type A records intact. Deletion of site specific records, for example, _ldap._tcp._&lt;SiteName&gt;._sites.dc._msdcs.&lt;DnsDomainName&gt;, is attempted for every site (&lt;SiteName&gt; in this example) in the enterprise of the domain controller on which the function is executed. Therefore, this function call could create a time-consuming run and may generate significant network traffic for enterprises with many sites.





> [!NOTE]
> The dsgetdc.h header defines DsDeregisterDnsHostRecords as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetdcsitecoveragea">DsGetDcSiteCoverage</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsgetsitenamea">DsGetSiteName</a>
