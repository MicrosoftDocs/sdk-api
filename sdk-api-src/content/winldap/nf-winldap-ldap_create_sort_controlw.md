---
UID: NF:winldap.ldap_create_sort_controlW
title: ldap_create_sort_controlW function (winldap.h)
description: The ldap_create_sort_controlW (Unicode) function (winldap.h) is used to format a list of sort keys into a search control.
helpviewer_keywords: ["_ldap_ldap_create_sort_control", "ldap.ldap__create__sort__control", "ldap.ldap_create_sort_control", "ldap_create_sort_control", "ldap_create_sort_control function [LDAP]", "ldap_create_sort_controlW", "winldap/ldap_create_sort_control", "winldap/ldap_create_sort_controlW"]
old-location: ldap\ldap_create_sort_control.htm
tech.root: ldap
ms.assetid: bbf8f860-ead8-4b22-8efa-0697076267ad
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_create_sort_control, ldap.ldap__create__sort__control, ldap.ldap_create_sort_control, ldap_create_sort_control, ldap_create_sort_control function [LDAP], ldap_create_sort_controlA, ldap_create_sort_controlW, winldap/ldap_create_sort_control, winldap/ldap_create_sort_controlA, winldap/ldap_create_sort_controlW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_create_sort_controlW (Unicode) and ldap_create_sort_controlA (ANSI)
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
 - ldap_create_sort_controlW
 - winldap/ldap_create_sort_controlW
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
 - ldap_create_sort_control
 - ldap_create_sort_controlA
 - ldap_create_sort_controlW
---

# ldap_create_sort_controlW function


## -description

The <b>ldap_create_sort_control</b> function is used to format a list of sort keys into a search control. Support for controls is available effective with LDAP 3, but whether the sort control is supported or not is dependent on the particular server.

## -parameters

### -param ExternalHandle [in]

The session handle.

### -param SortKeys [in]

Pointer to an array of 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a> structures. Each structure in the array specifies the name of an attribute to use as a sort key, the matching rule for that key, and whether the sort order is ascending or descending.

### -param IsCritical [in]

Notifies the server whether this control is critical to the search. 0 ==&gt; FALSE, !0 ==&gt; TRUE.

### -param Control [out]

Pointer to the newly created control.

## -returns

This function returns WINLDAPAPI ULONG LDAPAPI.

## -remarks

The <b>ldap_create_sort_control</b> function creates a basic sort control. Such a control is useful when the LDAP client has limited functionality and cannot sort results, yet needs them sorted.

The sort controls allow a server to return a result code for the sorting of the results that is independent of the result code returned for the search operation.

This function creates the control — it does not verify that  the server supports it, and consequently, does not return LDAP_UNAVAILABLE_CRIT_EXTENSION if the server does not support the control. However, it can return other standard LDAP return values, such as LDAP_NO_MEMORY or LDAP_PARAM_ERROR.

To free the control when it is no longer required, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_control_free">ldap_control_free</a>.





> [!NOTE]
> The winldap.h header defines ldap_create_sort_control as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a>



<a href="/previous-versions/windows/desktop/ldap/ldap-server-sort-oid">LDAP_SERVER_SORT_OID</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_control_free">ldap_control_free</a>
