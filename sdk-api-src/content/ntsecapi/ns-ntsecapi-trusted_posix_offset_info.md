---
UID: NS:ntsecapi._TRUSTED_POSIX_OFFSET_INFO
title: TRUSTED_POSIX_OFFSET_INFO
author: windows-sdk-content
description: Used to query or set the value used to generate Posix user and group identifiers.
old-location: security\trusted_posix_offset_info.htm
tech.root: secmgmt
ms.assetid: 0686da5e-43d4-49ac-8c5d-5c56b8d12e50
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PTRUSTED_POSIX_OFFSET_INFO, PTRUSTED_POSIX_OFFSET_INFO, PTRUSTED_POSIX_OFFSET_INFO structure pointer [Security], TRUSTED_POSIX_OFFSET_INFO, TRUSTED_POSIX_OFFSET_INFO structure [Security], _TRUSTED_POSIX_OFFSET_INFO, _lsa_trusted_posix_offset_info, ntsecapi/PTRUSTED_POSIX_OFFSET_INFO, ntsecapi/TRUSTED_POSIX_OFFSET_INFO, security.trusted_posix_offset_info"
ms.prod: windows-hardware
ms.technology: windows-devices
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
---

# TRUSTED_POSIX_OFFSET_INFO structure


## -description


The <b>TRUSTED_POSIX_OFFSET_INFO</b> structure is used to query or set the value used to generate Posix user and group identifiers. The 
<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a> and 
<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a> functions use this structure when their <i>InformationClass</i> parameters are set to <b>TrustedPosixOffsetInformation</b>.


## -struct-fields




### -field Offset

An offset that the system uses to generate Posix user and group identifiers that correspond to a given SID. To generate a Posix identifier, the system adds the RID from the SID to the Posix offset of the trusted domain identified by the SID.


## -see-also




<a href="https://msdn.microsoft.com/62925515-a6f3-4b5f-bf97-edb968af19a3">LsaQueryTrustedDomainInfo</a>



<a href="https://msdn.microsoft.com/a7b89ea7-af92-46ba-ac73-2fba1cc27680">LsaSetTrustedDomainInformation</a>



<a href="https://msdn.microsoft.com/442a0944-b498-4d9f-b338-d5aed1663d8d">TRUSTED_INFORMATION_CLASS</a>
 

 

