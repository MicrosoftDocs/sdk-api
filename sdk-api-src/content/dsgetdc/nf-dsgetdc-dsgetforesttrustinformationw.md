---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DsGetForestTrustInformationW function


## -description


The <b>DsGetForestTrustInformationW</b> function obtains forest trust data for a specified domain.


## -parameters




### -param OPTIONAL

TBD


### -param Flags [in]

Contains a set of flags that modify the behavior of this function. This can be zero or the following value.



#### DS_GFTI_UPDATE_TDO

If this flag is set, <b>DsGetForestTrustInformationW</b> will update
            the forest trust data of the trusted domain identified  by the <i>TrustedDomainName</i>
            parameter. In this case, the <i>TrustedDomainName</i> parameter cannot be <b>NULL</b>.
            The caller must have access to modify the trust data or
            <b>ERROR_ACCESS_DENIED</b> is returned.

This flag is only valid if <i>ServerName</i> specifies the primary domain controller of the domain.


### -param ForestTrustInfo [out]

Pointer to an <a href="https://msdn.microsoft.com/9e456462-59a9-4f18-ba47-92fc2350889b">LSA_FOREST_TRUST_INFORMATION</a> structure pointer that receives the forest trust data that describes the namespaces claimed by the
        domain specified by <i>TrustedDomainName</i>. The <b>Time</b>
        member of all returned records will be zero.

The caller must free this structure when it is no longer required by calling <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>.


#### - ServerName [in, optional]

Contains the name of the domain controller that <b>DsGetForestTrustInformationW</b> is connected to remotely.
        The caller must be an authenticated user on this server.
        If this parameter is <b>NULL</b>, the local server is used.


#### - TrustedDomainName [in, optional]

Contains the NETBIOS or DNS name of the trusted domain that the forest trust data
        is to be retrieved for.  This domain must have  the
        <b>TRUST_ATTRIBUTE_FOREST_TRANSITIVE</b> trust attribute. For more information, see <a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>.

If this parameter is <b>NULL</b>, the forest trust
        data for the domain hosted by <i>ServerName</i> is retrieved.


## -returns



Returns <b>NO_ERROR</b> if successful or a Win32 error code otherwise. Possible error codes include the following.




## -see-also




<a href="https://msdn.microsoft.com/7b519c81-5a6c-470a-a525-1894efd53305">Directory Service Functions</a>



<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a>



<a href="https://msdn.microsoft.com/acf9a2b5-f301-4e6a-a515-df338658ad56">TRUSTED_DOMAIN_INFORMATION_EX</a>
 

 

