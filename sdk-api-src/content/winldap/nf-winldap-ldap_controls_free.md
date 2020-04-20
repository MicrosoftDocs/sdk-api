---
UID: NF:winldap.ldap_controls_free
title: ldap_controls_free function (winldap.h)
description: Frees an array of LDAPControl structures.helpviewer_keywords: ["_ldap_ldap_controls_free","ldap.ldap__controls__free","ldap.ldap_controls_free","ldap_controls_free","ldap_controls_free function [LDAP]","ldap_controls_freeA","ldap_controls_freeW","winldap/ldap_controls_free","winldap/ldap_controls_freeA","winldap/ldap_controls_freeW"]
old-location: ldap\ldap_controls_free.htm
tech.root: ldap
ms.assetid: e1e4545f-6184-41bb-bba1-4eebae9cdaaf
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_controls_free, ldap.ldap__controls__free, ldap.ldap_controls_free, ldap_controls_free, ldap_controls_free function [LDAP], ldap_controls_freeA, ldap_controls_freeW, winldap/ldap_controls_free, winldap/ldap_controls_freeA, winldap/ldap_controls_freeW
f1_keywords:
- winldap/ldap_controls_free
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
req.unicode-ansi: ldap_controls_freeW (Unicode) and ldap_controls_freeA (ANSI)
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
- ldap_controls_free
- ldap_controls_freeA
- ldap_controls_freeW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_controls_free function


## -description


The <b>ldap_controls_free</b> function frees 
   an array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures.


## -parameters




### -param Controls [in]

The array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures to free.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
       <a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.




## -remarks



Use this function to free an array of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> 
     structures previously allocated by LDAP function calls, such as the array returned by 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>.

<div class="alert"><b>Note</b>  This function should only be used to free controls created internally by LDAP API functions. It is not used 
     to free memory that is explicitly allocated by the user application.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>
 

 

