---
UID: NF:aclapi.GetTrusteeNameW
title: GetTrusteeNameW function (aclapi.h)
description: Retrieves the trustee name from the specified TRUSTEE structure.helpviewer_keywords: ["GetTrusteeName","GetTrusteeName function [Security]","GetTrusteeNameA","GetTrusteeNameW","_win32_gettrusteename","aclapi/GetTrusteeName","aclapi/GetTrusteeNameA","aclapi/GetTrusteeNameW","security.gettrusteename"]
old-location: security\gettrusteename.htm
tech.root: SecAuthZ
ms.assetid: 9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6
ms.date: 12/05/2018
ms.keywords: GetTrusteeName, GetTrusteeName function [Security], GetTrusteeNameA, GetTrusteeNameW, _win32_gettrusteename, aclapi/GetTrusteeName, aclapi/GetTrusteeNameA, aclapi/GetTrusteeNameW, security.gettrusteename
f1_keywords:
- aclapi/GetTrusteeName
dev_langs:
- c++
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTrusteeNameW (Unicode) and GetTrusteeNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
api_name:
- GetTrusteeName
- GetTrusteeNameA
- GetTrusteeNameW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetTrusteeNameW function


## -description


The <b>GetTrusteeName</b> function retrieves the trustee name from the specified <a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.


## -parameters




### -param pTrustee [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.


## -returns



If the <b>TrusteeForm</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure is TRUSTEE_IS_NAME, the return value is the pointer assigned to the <b>ptstrName</b> member of the structure.

If the <b>TrusteeForm</b> member is TRUSTEE_IS_SID, the return value is <b>NULL</b>. The function does not look up the name associated with a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).




## -remarks



The <b>GetTrusteeName</b> function does not allocate any memory.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="https://docs.microsoft.com/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>
 

 

