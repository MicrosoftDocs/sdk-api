---
UID: NF:aclapi.GetTrusteeFormA
title: GetTrusteeFormA function (aclapi.h)
description: Retrieves the trustee name from the specified TRUSTEE structure. This value indicates whether the structure uses a name string or a security identifier (SID) to identify the trustee. (ANSI)
helpviewer_keywords: ["GetTrusteeFormA", "aclapi/GetTrusteeFormA"]
old-location: security\gettrusteeform.htm
tech.root: security
ms.assetid: e5e450b8-0b7b-4324-b453-5c020e74b1ee
ms.date: 12/05/2018
ms.keywords: GetTrusteeForm, GetTrusteeForm function [Security], GetTrusteeFormA, GetTrusteeFormW, _win32_gettrusteeform, aclapi/GetTrusteeForm, aclapi/GetTrusteeFormA, aclapi/GetTrusteeFormW, security.gettrusteeform
req.header: aclapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: GetTrusteeFormW (Unicode) and GetTrusteeFormA (ANSI)
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
 - GetTrusteeFormA
 - aclapi/GetTrusteeFormA
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
 - GetTrusteeForm
 - GetTrusteeFormA
 - GetTrusteeFormW
---

# GetTrusteeFormA function


## -description

The <b>GetTrusteeForm</b> function retrieves the trustee name from the specified <a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure. This value indicates whether the structure uses a name string or a <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) to identify the trustee.

## -parameters

### -param pTrustee [in]

A pointer to a 
<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a> structure.

## -returns

The return value is one of the constants from the 
<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_form">TRUSTEE_FORM</a> enumeration.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-control">Access Control Overview</a>



<a href="/windows/desktop/SecAuthZ/authorization-functions">Basic Access Control Functions</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-gettrusteenamea">GetTrusteeName</a>



<a href="/windows/desktop/api/aclapi/nf-aclapi-gettrusteetypea">GetTrusteeType</a>



<a href="/windows/desktop/api/accctrl/ns-accctrl-trustee_a">TRUSTEE</a>



<a href="/windows/desktop/api/accctrl/ne-accctrl-trustee_form">TRUSTEE_FORM</a>

## -remarks

> [!NOTE]
> The aclapi.h header defines GetTrusteeForm as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
