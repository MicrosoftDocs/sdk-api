---
UID: NF:aclapi.GetTrusteeNameW
title: GetTrusteeNameW function (aclapi.h)
description: Retrieves the trustee name from the specified TRUSTEE structure. (Unicode)
helpviewer_keywords: ["GetTrusteeName", "GetTrusteeName function [Security]", "GetTrusteeNameW", "_win32_gettrusteename", "aclapi/GetTrusteeName", "aclapi/GetTrusteeNameW", "security.gettrusteename"]
old-location: security\gettrusteename.htm
tech.root: security
ms.assetid: 9d3ce528-fb28-4e2e-bf7f-7d84c697fcb6
ms.date: 12/05/2018
ms.keywords: GetTrusteeName, GetTrusteeName function [Security], GetTrusteeNameA, GetTrusteeNameW, _win32_gettrusteename, aclapi/GetTrusteeName, aclapi/GetTrusteeNameA, aclapi/GetTrusteeNameW, security.gettrusteename
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetTrusteeNameW
 - aclapi/GetTrusteeNameW
dev_langs:
 - c++
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
---

# GetTrusteeNameW function


## -description

The <b>GetTrusteeName</b> function retrieves the trustee name from the specified <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -parameters

### -param pTrustee [in]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -returns

If the <b>TrusteeForm</b> member of the <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure is TRUSTEE_IS_NAME, the return value is the pointer assigned to the <b>ptstrName</b> member of the structure.

If the <b>TrusteeForm</b> member is TRUSTEE_IS_SID, the return value is <b>NULL</b>. The function does not look up the name associated with a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID).

## -remarks

The <b>GetTrusteeName</b> function does not allocate any memory.





> [!NOTE]
> The aclapi.h header defines GetTrusteeName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>
