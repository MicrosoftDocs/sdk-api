---
UID: NS:ntsecapi._POLICY_MODIFICATION_INFO
title: "_POLICY_MODIFICATION_INFO"
author: windows-sdk-content
description: The POLICY_MODIFICATION_INFO structure is used to query information about the creation time and last modification of the LSA database.
old-location: security\policy_modification_info.htm
old-project: secmgmt
ms.assetid: ef4d1d1d-9b1b-4d67-80b8-2b548ec31a87
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPOLICY_MODIFICATION_INFO, POLICY_MODIFICATION_INFO, POLICY_MODIFICATION_INFO structure [Security], PPOLICY_MODIFICATION_INFO, PPOLICY_MODIFICATION_INFO structure pointer [Security], _POLICY_MODIFICATION_INFO, _lsa_policy_modification_info, ntsecapi/POLICY_MODIFICATION_INFO, ntsecapi/PPOLICY_MODIFICATION_INFO, security.policy_modification_info"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: POLICY_MODIFICATION_INFO, *PPOLICY_MODIFICATION_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - POLICY_MODIFICATION_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _POLICY_MODIFICATION_INFO structure


## -description


The <b>POLICY_MODIFICATION_INFO</b> structure is used to query information about the creation time and last modification of the LSA database. The 
<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a> function uses this structure when its <i>InformationClass</i> parameter is set to PolicyModificationInformation.


## -struct-fields




### -field ModifiedId

A 
<a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure containing a 64-bit unsigned integer that is incremented each time anything in the LSA database is modified. This value is modified only on primary domain controllers.


### -field DatabaseCreationTime

A <a href="https://msdn.microsoft.com/6a2985b6-5baf-49ab-af28-67c1374557ea">LARGE_INTEGER</a> structure that indicates the date and time the LSA database was created. This is a UTC-based time that uses the <a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a> format. On backup domain controllers, this value is replicated from the primary domain controller. For more information about UTC-based time, see 
<a href="https://msdn.microsoft.com/1a1e251e-2375-4134-bbd8-1e4670b9f9d2">System Time</a>.


## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/2d543500-f639-4ef7-91f4-cdc5060dd567">LsaQueryInformationPolicy</a>



<a href="https://msdn.microsoft.com/2aa3b09e-2cd9-4a09-bfd6-b37c97266dcb">LsaSetInformationPolicy</a>



<a href="https://msdn.microsoft.com/b734b5e8-1ee9-436b-b2a9-210ae79fbaf5">POLICY_INFORMATION_CLASS</a>
 

 

