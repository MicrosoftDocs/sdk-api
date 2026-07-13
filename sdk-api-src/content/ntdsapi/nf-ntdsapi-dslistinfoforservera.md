---
UID: NF:ntdsapi.DsListInfoForServerA
title: DsListInfoForServerA function (ntdsapi.h)
description: The DsListInfoForServer function lists miscellaneous data for a server. (ANSI)
helpviewer_keywords: ["DS_LIST_ACCOUNT_OBJECT_FOR_SERVER", "DS_LIST_DNS_HOST_NAME_FOR_SERVER", "DS_LIST_DSA_OBJECT_FOR_SERVER", "DsListInfoForServerA", "ntdsapi/DsListInfoForServerA"]
old-location: ad\dslistinfoforserver.htm
tech.root: ad
ms.assetid: 15dcc7ac-4edb-42fa-8466-033794762046
ms.date: 12/05/2018
ms.keywords: DS_LIST_ACCOUNT_OBJECT_FOR_SERVER, DS_LIST_DNS_HOST_NAME_FOR_SERVER, DS_LIST_DSA_OBJECT_FOR_SERVER, DsListInfoForServer, DsListInfoForServer function [Active Directory], DsListInfoForServerA, DsListInfoForServerW, _glines_dslistinfoforserver, ad.dslistinfoforserver, ntdsapi/DsListInfoForServer, ntdsapi/DsListInfoForServerA, ntdsapi/DsListInfoForServerW
req.header: ntdsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DsListInfoForServerW (Unicode) and DsListInfoForServerA (ANSI)
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
 - DsListInfoForServerA
 - ntdsapi/DsListInfoForServerA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdsapi.dll
api_name:
 - DsListInfoForServer
 - DsListInfoForServerA
 - DsListInfoForServerW
---

# DsListInfoForServerA function


## -description

The <b>DsListInfoForServer</b> function lists miscellaneous data for a server.

## -parameters

### -param hDs [in]

Contains a directory service handle obtained from either the 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbinda">DSBind</a> or 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsbindwithcreda">DSBindWithCred</a> function.

### -param server [in]

Pointer to a null-terminated string that specifies the server name. This name must be the same as one of the strings returned by the <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea">DsListServersForDomainInSite</a> or <a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dslistserversinsitea">DsListServersInSite</a> function.

### -param ppInfo [out]

Pointer to a variable that receives a pointer to a 
<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure that contains the server data. The returned structure must be deallocated using 
<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>.

The indexes of the array in the <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure indicate what data are contained by each array element. The following constants may be used to specify the desired index for a particular piece of data.



#### DS_LIST_ACCOUNT_OBJECT_FOR_SERVER

Name of the account object for the domain controller (DC).



#### DS_LIST_DNS_HOST_NAME_FOR_SERVER

DNS host name of the DC.



#### DS_LIST_DSA_OBJECT_FOR_SERVER

GUID of the directory service agent (DSA) for the domain controller (DC).

## -returns

If the function returns server data, the return value is <b>NO_ERROR</b>.

If the function fails, the return value can be one of the following error codes.

## -remarks

Individual name conversion errors are reported in the returned <a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a> structure.





> [!NOTE]
> The ntdsapi.h header defines DsListInfoForServer as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/ntdsapi/ns-ntdsapi-ds_name_resulta">DS_NAME_RESULT</a>



<a href="/windows/desktop/AD/dc-and-replication-management-functions">Domain Controller and Replication Management Functions</a>



<a href="/windows/desktop/api/ntdsapi/nf-ntdsapi-dsfreenameresulta">DsFreeNameResult</a>
