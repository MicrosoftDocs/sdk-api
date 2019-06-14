---
UID: NS:ntsecapi._TRUSTED_POSIX_OFFSET_INFO
title: TRUSTED_POSIX_OFFSET_INFO (ntsecapi.h)
author: windows-sdk-content
description: Used to query or set the value used to generate Posix user and group identifiers.
old-location: security\trusted_posix_offset_info.htm
tech.root: SecMgmt
ms.assetid: 0686da5e-43d4-49ac-8c5d-5c56b8d12e50
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PTRUSTED_POSIX_OFFSET_INFO, PTRUSTED_POSIX_OFFSET_INFO, PTRUSTED_POSIX_OFFSET_INFO structure pointer [Security], TRUSTED_POSIX_OFFSET_INFO, TRUSTED_POSIX_OFFSET_INFO structure [Security], _TRUSTED_POSIX_OFFSET_INFO, _lsa_trusted_posix_offset_info, ntsecapi/PTRUSTED_POSIX_OFFSET_INFO, ntsecapi/TRUSTED_POSIX_OFFSET_INFO, security.trusted_posix_offset_info"
ms.topic: struct
req.header: ntsecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - TRUSTED_POSIX_OFFSET_INFO
product: Windows
targetos: Windows
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
req.redist: 
ms.custom: 19H1
---

# TRUSTED_POSIX_OFFSET_INFO structure


## -description


The <b>TRUSTED_POSIX_OFFSET_INFO</b> structure is used to query or set the value used to generate Posix user and group identifiers. The 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>TrustedPosixOffsetInformation</b>.


## -struct-fields




### -field Offset

An offset that the system uses to generate Posix user and group identifiers that correspond to a given SID. To generate a Posix identifier, the system adds the RID from the SID to the Posix offset of the trusted domain identified by the SID.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaquerytrusteddomaininfo">LsaQueryTrustedDomainInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasettrusteddomaininformation">LsaSetTrustedDomainInformation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/ne-ntsecapi-_trusted_information_class">TRUSTED_INFORMATION_CLASS</a>
 

 

