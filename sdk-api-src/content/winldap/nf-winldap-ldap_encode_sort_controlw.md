---
UID: NF:winldap.ldap_encode_sort_controlW
title: ldap_encode_sort_controlW function (winldap.h)
description: The ldap_encode_sort_controlW (Unicode) function formats a list of sort keys into a search control. This function is obsolete, use the ldap_create_sort_controlW (Unicode) function instead.
helpviewer_keywords: ["_ldap_ldap_encode_sort_control", "ldap.ldap__encode__sort__control", "ldap.ldap_encode_sort_control", "ldap_encode_sort_control", "ldap_encode_sort_control function [LDAP]", "ldap_encode_sort_controlW", "winldap/ldap_encode_sort_control", "winldap/ldap_encode_sort_controlW"]
old-location: ldap\ldap_encode_sort_control.htm
tech.root: ldap
ms.assetid: 5c6c3bd4-739f-413d-adc3-668ac7b56da6
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_encode_sort_control, ldap.ldap__encode__sort__control, ldap.ldap_encode_sort_control, ldap_encode_sort_control, ldap_encode_sort_control function [LDAP], ldap_encode_sort_controlA, ldap_encode_sort_controlW, winldap/ldap_encode_sort_control, winldap/ldap_encode_sort_controlA, winldap/ldap_encode_sort_controlW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_encode_sort_controlW (Unicode) and ldap_encode_sort_controlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ldap_encode_sort_controlW
 - winldap/ldap_encode_sort_controlW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ldap_encode_sort_control
 - ldap_encode_sort_controlA
 - ldap_encode_sort_controlW
---

# ldap_encode_sort_controlW function


## -description

The <b>ldap_encode_sort_control</b> function formats a list of sort keys into a search control. This function is obsolete. Instead, use 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param SortKeys [in]

A list of 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a> structures.

### -param Control [out]

Pointer to the new control.

### -param Criticality [in]

Notifies the server whether this control is critical to the search.

## -returns

If the call completed successfully, <b>LDAP_SUCCESS</b> is returned. Other standard LDAP return values, such as <b>LDAP_NO_MEMORY</b> or <b>LDAP_PARAM_ERROR</b>, may also be returned.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>

## -remarks

> [!NOTE]
> The winldap.h header defines ldap_encode_sort_control as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
