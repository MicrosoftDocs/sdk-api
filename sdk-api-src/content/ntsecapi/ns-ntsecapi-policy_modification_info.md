---
UID: NS:ntsecapi._POLICY_MODIFICATION_INFO
title: POLICY_MODIFICATION_INFO (ntsecapi.h)
description: The POLICY_MODIFICATION_INFO structure is used to query information about the creation time and last modification of the LSA database.
helpviewer_keywords: ["*PPOLICY_MODIFICATION_INFO","POLICY_MODIFICATION_INFO","POLICY_MODIFICATION_INFO structure [Security]","PPOLICY_MODIFICATION_INFO","PPOLICY_MODIFICATION_INFO structure pointer [Security]","_POLICY_MODIFICATION_INFO","_lsa_policy_modification_info","ntsecapi/POLICY_MODIFICATION_INFO","ntsecapi/PPOLICY_MODIFICATION_INFO","security.policy_modification_info"]
old-location: security\policy_modification_info.htm
tech.root: security
ms.assetid: ef4d1d1d-9b1b-4d67-80b8-2b548ec31a87
ms.date: 12/05/2018
ms.keywords: '*PPOLICY_MODIFICATION_INFO, POLICY_MODIFICATION_INFO, POLICY_MODIFICATION_INFO structure [Security], PPOLICY_MODIFICATION_INFO, PPOLICY_MODIFICATION_INFO structure pointer [Security], _POLICY_MODIFICATION_INFO, _lsa_policy_modification_info, ntsecapi/POLICY_MODIFICATION_INFO, ntsecapi/PPOLICY_MODIFICATION_INFO, security.policy_modification_info'
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
targetos: Windows
req.typenames: POLICY_MODIFICATION_INFO, *PPOLICY_MODIFICATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _POLICY_MODIFICATION_INFO
 - ntsecapi/_POLICY_MODIFICATION_INFO
 - PPOLICY_MODIFICATION_INFO
 - ntsecapi/PPOLICY_MODIFICATION_INFO
 - POLICY_MODIFICATION_INFO
 - ntsecapi/POLICY_MODIFICATION_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecapi.h
api_name:
 - POLICY_MODIFICATION_INFO
---

# POLICY_MODIFICATION_INFO structure


## -description

The <b>POLICY_MODIFICATION_INFO</b> structure is used to query information about the creation time and last modification of the LSA database. The 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a> function uses this structure when its <i>InformationClass</i> parameter is set to PolicyModificationInformation.

## -struct-fields

### -field ModifiedId

A 
<a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure containing a 64-bit unsigned integer that is incremented each time anything in the LSA database is modified. This value is modified only on primary domain controllers.

### -field DatabaseCreationTime

A <a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a> structure that indicates the date and time the LSA database was created. This is a UTC-based time that uses the <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> format. On backup domain controllers, this value is replicated from the primary domain controller. For more information about UTC-based time, see 
<a href="/windows/desktop/SysInfo/system-time">System Time</a>.

## -see-also

<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaqueryinformationpolicy">LsaQueryInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsasetinformationpolicy">LsaSetInformationPolicy</a>



<a href="/windows/desktop/api/ntsecapi/ne-ntsecapi-policy_information_class">POLICY_INFORMATION_CLASS</a>