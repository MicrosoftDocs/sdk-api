---
UID: NF:winldap.ldap_parse_page_control
title: ldap_parse_page_control function (winldap.h)
description: The ldap_parse_page_control parses the results of a search into pages.helpviewer_keywords: ["_ldap_ldap_parse_page_control","ldap.ldap__parse__page__control","ldap.ldap_parse_page_control","ldap_parse_page_control","ldap_parse_page_control function [LDAP]","ldap_parse_page_controlA","ldap_parse_page_controlW","winldap/ldap_parse_page_control","winldap/ldap_parse_page_controlA","winldap/ldap_parse_page_controlW"]
old-location: ldap\ldap_parse_page_control.htm
tech.root: ldap
ms.assetid: babf74d1-2f9c-40f8-ba82-e298e49ad937
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_parse_page_control, ldap.ldap__parse__page__control, ldap.ldap_parse_page_control, ldap_parse_page_control, ldap_parse_page_control function [LDAP], ldap_parse_page_controlA, ldap_parse_page_controlW, winldap/ldap_parse_page_control, winldap/ldap_parse_page_controlA, winldap/ldap_parse_page_controlW
f1_keywords:
- winldap/ldap_parse_page_control
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
req.unicode-ansi: ldap_parse_page_controlW (Unicode) and ldap_parse_page_controlA (ANSI)
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
- ldap_parse_page_control
- ldap_parse_page_controlA
- ldap_parse_page_controlW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_parse_page_control function


## -description


The <b>ldap_parse_page_control</b> parses the results of a search into pages.


## -parameters




### -param ExternalHandle [in]

The session handle.


### -param ServerControls [in]

An array of controls that includes a page control. The page control contains the cookie and total count fields returned by the server.


### -param TotalCount [out]

A pointer to the total count of entries returned in this page (optional).


### -param Cookie [out]

An opaque cookie, used by the server to determine its location in the result set. Use ber_bvfree to free.


## -returns



If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. See 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.




## -remarks



Use <b>ldap_parse_page_control</b> in conjunction with 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_page_control">ldap_create_page_control</a> and 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a> to implement the simple paging of results by means of controls. After calling <b>ldap_parse_page_control</b> to retrieve the server controls and extract the cookie from the search result, call <b>ldap_parse_result</b> to parse the results. Then use the cookie to call <b>ldap_create_page_control</b> to retrieve the next page of results.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_page_control">ldap_create_page_control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>
 

 

