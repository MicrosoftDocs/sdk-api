---
UID: NS:ntsecapi._LSA_ENUMERATION_INFORMATION
title: "_LSA_ENUMERATION_INFORMATION"
author: windows-sdk-content
description: The LSA_ENUMERATION_INFORMATION structure is used with the LsaEnumerateAccountsWithUserRight function to return a pointer to a SID.
old-location: security\lsa_enumeration_information.htm
tech.root: secmgmt
ms.assetid: 7577548f-3ceb-43a5-b447-6f66a09963fe
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PLSA_ENUMERATION_INFORMATION, LSA_ENUMERATION_INFORMATION, LSA_ENUMERATION_INFORMATION structure [Security], PLSA_ENUMERATION_INFORMATION, PLSA_ENUMERATION_INFORMATION structure pointer [Security], _LSA_ENUMERATION_INFORMATION, _lsa_lsa_enumeration_information, ntsecapi/LSA_ENUMERATION_INFORMATION, ntsecapi/PLSA_ENUMERATION_INFORMATION, security.lsa_enumeration_information"
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
 - LSA_ENUMERATION_INFORMATION
product: Windows
targetos: Windows
req.typenames: LSA_ENUMERATION_INFORMATION, *PLSA_ENUMERATION_INFORMATION
req.redist: 
---

# _LSA_ENUMERATION_INFORMATION structure


## -description


The <b>LSA_ENUMERATION_INFORMATION</b> structure is used with the 
<a href="https://msdn.microsoft.com/97e7180e-4edb-4edd-915e-0477e7e7a9ff">LsaEnumerateAccountsWithUserRight</a> function to return a pointer to a SID.


## -struct-fields




### -field Sid

Pointer to a SID.


## -see-also




<a href="https://msdn.microsoft.com/97e7180e-4edb-4edd-915e-0477e7e7a9ff">LsaEnumerateAccountsWithUserRight</a>
 

 

