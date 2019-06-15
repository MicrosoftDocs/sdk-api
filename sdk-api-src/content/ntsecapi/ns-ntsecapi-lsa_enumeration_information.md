---
UID: NS:ntsecapi._LSA_ENUMERATION_INFORMATION
title: LSA_ENUMERATION_INFORMATION (ntsecapi.h)
author: windows-sdk-content
description: The LSA_ENUMERATION_INFORMATION structure is used with the LsaEnumerateAccountsWithUserRight function to return a pointer to a SID.
old-location: security\lsa_enumeration_information.htm
tech.root: SecMgmt
ms.assetid: 7577548f-3ceb-43a5-b447-6f66a09963fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PLSA_ENUMERATION_INFORMATION, LSA_ENUMERATION_INFORMATION, LSA_ENUMERATION_INFORMATION structure [Security], PLSA_ENUMERATION_INFORMATION, PLSA_ENUMERATION_INFORMATION structure pointer [Security], _LSA_ENUMERATION_INFORMATION, _lsa_lsa_enumeration_information, ntsecapi/LSA_ENUMERATION_INFORMATION, ntsecapi/PLSA_ENUMERATION_INFORMATION, security.lsa_enumeration_information"
ms.topic: struct
f1_keywords: ["ntsecapi/LSA_ENUMERATION_INFORMATION"]
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
 - LSA_ENUMERATION_INFORMATION
product: Windows
targetos: Windows
req.typenames: LSA_ENUMERATION_INFORMATION, *PLSA_ENUMERATION_INFORMATION
req.redist: 
ms.custom: 19H1
---

# LSA_ENUMERATION_INFORMATION structure


## -description


The <b>LSA_ENUMERATION_INFORMATION</b> structure is used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright">LsaEnumerateAccountsWithUserRight</a> function to return a pointer to a SID.


## -struct-fields




### -field Sid

Pointer to a SID.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumerateaccountswithuserright">LsaEnumerateAccountsWithUserRight</a>
 

 

