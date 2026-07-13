---
UID: NF:dsgetdc.DsEnumerateDomainTrustsW
title: DsEnumerateDomainTrustsW function (dsgetdc.h)
description: Obtains domain trust data for a specified domain. (Unicode)
helpviewer_keywords: ["DS_DOMAIN_DIRECT_INBOUND", "DS_DOMAIN_DIRECT_OUTBOUND", "DS_DOMAIN_IN_FOREST", "DS_DOMAIN_NATIVE_MODE", "DS_DOMAIN_PRIMARY", "DS_DOMAIN_TREE_ROOT", "DsEnumerateDomainTrusts", "DsEnumerateDomainTrusts function [Active Directory]", "DsEnumerateDomainTrustsW", "_glines_dsenumeratedomaintrusts", "ad.dsenumeratedomaintrusts", "dsgetdc/DsEnumerateDomainTrusts", "dsgetdc/DsEnumerateDomainTrustsW"]
old-location: ad\dsenumeratedomaintrusts.htm
tech.root: ad
ms.assetid: 6c3b788f-ee53-4637-acdb-04316e8464fe
ms.date: 12/05/2018
ms.keywords: DS_DOMAIN_DIRECT_INBOUND, DS_DOMAIN_DIRECT_OUTBOUND, DS_DOMAIN_IN_FOREST, DS_DOMAIN_NATIVE_MODE, DS_DOMAIN_PRIMARY, DS_DOMAIN_TREE_ROOT, DsEnumerateDomainTrusts, DsEnumerateDomainTrusts function [Active Directory], DsEnumerateDomainTrustsA, DsEnumerateDomainTrustsW, _glines_dsenumeratedomaintrusts, ad.dsenumeratedomaintrusts, dsgetdc/DsEnumerateDomainTrusts, dsgetdc/DsEnumerateDomainTrustsA, dsgetdc/DsEnumerateDomainTrustsW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsEnumerateDomainTrustsW (Unicode) and DsEnumerateDomainTrustsA (ANSI)
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
 - DsEnumerateDomainTrustsW
 - dsgetdc/DsEnumerateDomainTrustsW
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
 - DsEnumerateDomainTrusts
 - DsEnumerateDomainTrustsA
 - DsEnumerateDomainTrustsW
---

# DsEnumerateDomainTrustsW function


## -description

The <b>DsEnumerateDomainTrusts</b> function obtains domain trust data for a specified domain.

## -parameters

### -param ServerName [in, optional]

Pointer to a null-terminated string that specifies the name of a computer in the domain to obtain the trust information for. If this parameter is <b>NULL</b>, the name of the local computer is used. The caller must be an authenticated user in this domain.

If this computer is a domain controller, this function returns the trust data immediately. If this computer is not a domain controller, this function  obtains the trust data  from cached data if the cached data is not expired. If the cached data is expired, this function obtains the trust data from a domain controller in the domain that this computer is a member of and updates the cache. The cached data automatically expires after five minutes.

### -param Flags [in]

Contains a set of flags that determines which domain trusts to enumerate. This can be zero or a combination of one or more of the following values.



#### DS_DOMAIN_DIRECT_INBOUND

Enumerate domains that directly trust the domain which has <i>ServerName</i> as a member.



#### DS_DOMAIN_DIRECT_OUTBOUND

Enumerate domains directly trusted by the domain which has <i>ServerName</i> as a member.



#### DS_DOMAIN_IN_FOREST

Enumerate domains that are a member of the same forest which has <i>ServerName</i> as a member.



#### DS_DOMAIN_NATIVE_MODE

Enumerate domains where the primary domain is running in Windows 2000 native mode.



#### DS_DOMAIN_PRIMARY

Enumerate domains that are the primary domain of the domain which has <i>ServerName</i> as a member.



#### DS_DOMAIN_TREE_ROOT

Enumerate domains that are at the root of the forest which has <i>ServerName</i> as a member.

### -param Domains [out]

Pointer to a <b>PDS_DOMAIN_TRUSTS</b> value that receives an array of <a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-ds_domain_trustsa">DS_DOMAIN_TRUSTS</a> structures. Each structure in this array contains trust data about a domain. The caller must free this memory when it is no longer required by calling <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.

### -param DomainCount [out]

Pointer to a <b>ULONG</b> value that receives the number of elements returned in the <i>Domains</i> array.


##### - Flags.DS_DOMAIN_DIRECT_INBOUND

Enumerate domains that directly trust the domain which has <i>ServerName</i> as a member.


##### - Flags.DS_DOMAIN_DIRECT_OUTBOUND

Enumerate domains directly trusted by the domain which has <i>ServerName</i> as a member.


##### - Flags.DS_DOMAIN_IN_FOREST

Enumerate domains that are a member of the same forest which has <i>ServerName</i> as a member.


##### - Flags.DS_DOMAIN_NATIVE_MODE

Enumerate domains where the primary domain is running in Windows 2000 native mode.


##### - Flags.DS_DOMAIN_PRIMARY

Enumerate domains that are the primary domain of the domain which has <i>ServerName</i> as a member.


##### - Flags.DS_DOMAIN_TREE_ROOT

Enumerate domains that are at the root of the forest which has <i>ServerName</i> as a member.

## -returns

Returns <b>ERROR_SUCCESS</b> if successful or a Win32 error code otherwise. Possible error codes include those listed in the following list.

## -see-also

<a href="/windows/desktop/api/dsgetdc/ns-dsgetdc-ds_domain_trustsa">DS_DOMAIN_TRUSTS</a>



<a href="/windows/desktop/AD/directory-service-functions">Directory Service
    Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>

## -remarks

> [!NOTE]
> The dsgetdc.h header defines DsEnumerateDomainTrusts as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
