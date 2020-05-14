---
UID: NF:winldap.ldap_create_page_controlA
title: ldap_create_page_controlA function (winldap.h)
description: Use the ldap_create_page_control function to create a basic control for paging results. Support for controls is available effective with LDAP 3, but whether the page control is supported or not is dependent on the particular server.
helpviewer_keywords: ["_ldap_ldap_create_page_control","ldap.ldap__create__page__control","ldap.ldap_create_page_control","ldap_create_page_control","ldap_create_page_control function [LDAP]","ldap_create_page_controlA","ldap_create_page_controlW","winldap/ldap_create_page_control","winldap/ldap_create_page_controlA","winldap/ldap_create_page_controlW"]
old-location: ldap\ldap_create_page_control.htm
tech.root: ldap
ms.assetid: b3b1f3bd-7eb3-4f76-921c-386562dae2e2
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_create_page_control, ldap.ldap__create__page__control, ldap.ldap_create_page_control, ldap_create_page_control, ldap_create_page_control function [LDAP], ldap_create_page_controlA, ldap_create_page_controlW, winldap/ldap_create_page_control, winldap/ldap_create_page_controlA, winldap/ldap_create_page_controlW
f1_keywords:
- winldap/ldap_create_page_control
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
req.unicode-ansi: ldap_create_page_controlW (Unicode) and ldap_create_page_controlA (ANSI)
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
- ldap_create_page_control
- ldap_create_page_controlA
- ldap_create_page_controlW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_create_page_controlA function


## -description


Use the <b>ldap_create_page_control</b> function to create a basic control for paging results. Support for controls is available effective with LDAP 3, but whether the page control is supported or not is dependent on the particular server.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param PageSize [in]

The number of entries to return in each page.


### -param Cookie [in]

Pointer to a 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure that the server uses to determine its location in the result set. This is an opaque structure that you should not access directly. Set to <b>NULL</b> for the first call to <b>ldap_create_page_control</b>.


### -param IsCritical [in]

Notifies the server whether this control is critical to the search.


### -param Control [out]

Pointer to the newly created control.


## -returns



This function returns WINLDAPAPI ULONG LDAPAPI.




## -remarks



The <b>ldap_create_page_control</b> function creates a simple paged-results control. The control enables the client to specify the rate at which an LDAP server returns the results of a search operation. This is useful when the client has limited resources and may not be able to process the entire result set from a given LDAP query, or when the client/server connection is slow.

To create the paged-results control, specify the number of entries to be returned in a single page. To return results normally, even if it cannot support this control, set the <i>IsCritical</i> parameter to <b>FALSE</b>.

This function creates the control - it does not verify that the server supports it, and consequently, does not return <b>LDAP_UNAVAILABLE_CRIT_EXTENSION</b> if the server does not support the control. However, it can return other standard LDAP return values, such as <b>LDAP_NO_MEMORY</b> or <b>LDAP_PARAM_ERROR</b>.

When <b>ldap_create_page_control</b> returns successfully, include the newly created control to the list of server controls in a call to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a> or to 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>. When the server returns the first page of results, call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a> to retrieve the first page of results.

Call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_control_free">ldap_control_free</a> when the control is no longer required.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-paged-result-oid-string">LDAP_PAGED_RESULT_OID_STRING</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_control_free">ldap_control_free</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_page_control">ldap_parse_page_control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>
 

 

