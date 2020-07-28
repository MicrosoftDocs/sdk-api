---
UID: NF:winldap.ldap_encode_sort_controlA
title: ldap_encode_sort_controlA function (winldap.h)
description: The ldap_encode_sort_control function formats a list of sort keys into a search control. This function is obsolete. Instead, use ldap_create_sort_control.
helpviewer_keywords: ["_ldap_ldap_encode_sort_control","ldap.ldap__encode__sort__control","ldap.ldap_encode_sort_control","ldap_encode_sort_control","ldap_encode_sort_control function [LDAP]","ldap_encode_sort_controlA","ldap_encode_sort_controlW","winldap/ldap_encode_sort_control","winldap/ldap_encode_sort_controlA","winldap/ldap_encode_sort_controlW"]
old-location: ldap\ldap_encode_sort_control.htm
tech.root: ldap
ms.assetid: 5c6c3bd4-739f-413d-adc3-668ac7b56da6
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_encode_sort_control, ldap.ldap__encode__sort__control, ldap.ldap_encode_sort_control, ldap_encode_sort_control, ldap_encode_sort_control function [LDAP], ldap_encode_sort_controlA, ldap_encode_sort_controlW, winldap/ldap_encode_sort_control, winldap/ldap_encode_sort_controlA, winldap/ldap_encode_sort_controlW
f1_keywords:
- winldap/ldap_encode_sort_control
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_encode_sort_controlA function


## -description


The <b>ldap_encode_sort_control</b> function formats a list of sort keys into a search control. This function is obsolete. Instead, use 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param SortKeys [in]

A list of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a> structures.


### -param Control [out]

Pointer to the new control.


### -param Criticality [in]

Notifies the server whether this control is critical to the search.


## -returns



If the call completed successfully, <b>LDAP_SUCCESS</b> is returned. Other standard LDAP return values, such as <b>LDAP_NO_MEMORY</b> or <b>LDAP_PARAM_ERROR</b>, may also be returned.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapsortkeya">LDAPSortKey</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>
 

 

