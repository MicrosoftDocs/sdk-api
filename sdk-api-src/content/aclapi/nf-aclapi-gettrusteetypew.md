---
UID: NF:aclapi.GetTrusteeTypeW
title: GetTrusteeTypeW function (aclapi.h)
description: Retrieves the trustee type from the specified TRUSTEE structure. This value indicates whether the trustee is a user, a group, or the trustee type is unknown. (Unicode)
helpviewer_keywords: ["GetTrusteeType", "GetTrusteeType function [Security]", "GetTrusteeTypeW", "_win32_gettrusteetype", "aclapi/GetTrusteeType", "aclapi/GetTrusteeTypeW", "security.gettrusteetype"]
old-location: security\gettrusteetype.htm
tech.root: security
ms.assetid: 19777929-43cf-45ea-8283-e42bf9ce8d7a
ms.date: 12/05/2018
ms.keywords: GetTrusteeType, GetTrusteeType function [Security], GetTrusteeTypeA, GetTrusteeTypeW, _win32_gettrusteetype, aclapi/GetTrusteeType, aclapi/GetTrusteeTypeA, aclapi/GetTrusteeTypeW, security.gettrusteetype
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTrusteeTypeW (Unicode) and GetTrusteeTypeA (ANSI)
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
 - GetTrusteeTypeW
 - aclapi/GetTrusteeTypeW
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
 - GetTrusteeType
 - GetTrusteeTypeA
 - GetTrusteeTypeW
---

# GetTrusteeTypeW function


## -description

The <b>GetTrusteeType</b> function retrieves the trustee type from the specified <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. This value indicates whether the trustee is a user, a group, or the trustee type is unknown.

## -parameters

### -param pTrustee [in, optional]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -returns

The return value is one of the constants from the <a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_type">TRUSTEE_TYPE</a> enumeration.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_type">TRUSTEE_TYPE</a>

## -remarks

> [!NOTE]
> The aclapi.h header defines GetTrusteeType as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
