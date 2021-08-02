---
UID: NF:dsgetdc.DsGetForestTrustInformationW
title: DsGetForestTrustInformationW function (dsgetdc.h)
description: Obtains forest trust data for a specified domain.
helpviewer_keywords: ["DS_GFTI_UPDATE_TDO","DsGetForestTrustInformationW","DsGetForestTrustInformationW function [Active Directory]","ad.dsgetforesttrustinformationw","dsgetdc/DsGetForestTrustInformationW"]
old-location: ad\dsgetforesttrustinformationw.htm
tech.root: ad
ms.assetid: c94fdc5b-920b-4807-9cbf-3172ec1c7386
ms.date: 12/05/2018
ms.keywords: DS_GFTI_UPDATE_TDO, DsGetForestTrustInformationW, DsGetForestTrustInformationW function [Active Directory], ad.dsgetforesttrustinformationw, dsgetdc/DsGetForestTrustInformationW
req.header: dsgetdc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - DsGetForestTrustInformationW
 - dsgetdc/DsGetForestTrustInformationW
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
 - DsGetForestTrustInformationW
---

# DsGetForestTrustInformationW function


## -description

The <b>DsGetForestTrustInformationW</b> function obtains forest trust data for a specified domain.

## -parameters

### -param ServerName [in, optional]

Contains the name of the domain controller that <b>DsGetForestTrustInformationW</b> is connected to remotely.
        The caller must be an authenticated user on this server.
        If this parameter is <b>NULL</b>, the local server is used.

### -param TrustedDomainName [in, optional]

Contains the NETBIOS or DNS name of the trusted domain that the forest trust data
        is to be retrieved for.  This domain must have  the
        <b>TRUST_ATTRIBUTE_FOREST_TRANSITIVE</b> trust attribute. For more information, see <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>.

If this parameter is <b>NULL</b>, the forest trust
        data for the domain hosted by <i>ServerName</i> is retrieved.

### -param Flags [in]

Contains a set of flags that modify the behavior of this function. This can be zero or the following value.



#### DS_GFTI_UPDATE_TDO

If this flag is set, <b>DsGetForestTrustInformationW</b> will update
            the forest trust data of the trusted domain identified  by the <i>TrustedDomainName</i> parameter. In this case, the <i>TrustedDomainName</i> parameter cannot be <b>NULL</b>.
            The caller must have access to modify the trust data or
            <b>ERROR_ACCESS_DENIED</b> is returned.

This flag is only valid if <i>ServerName</i> specifies the primary domain controller of the domain.

### -param ForestTrustInfo [out]

Pointer to an <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-lsa_forest_trust_information">LSA_FOREST_TRUST_INFORMATION</a> structure pointer that receives the forest trust data that describes the namespaces claimed by the
        domain specified by <i>TrustedDomainName</i>. The <b>Time</b> member of all returned records will be zero.

The caller must free this structure when it is no longer required by calling <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>.

## -returns

Returns <b>NO_ERROR</b> if successful or a Win32 error code otherwise. Possible error codes include the following.

## -see-also

<a href="/windows/desktop/AD/directory-service-functions">Directory Service Functions</a>



<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a>



<a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-trusted_domain_information_ex">TRUSTED_DOMAIN_INFORMATION_EX</a>