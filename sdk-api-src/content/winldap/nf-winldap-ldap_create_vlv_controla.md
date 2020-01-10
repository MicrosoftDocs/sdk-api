---
UID: NF:winldap.ldap_create_vlv_controlA
title: ldap_create_vlv_controlA function (winldap.h)
description: The ldap_create_vlv_control function is used to create the request control (LDAP_CONTROL_VLVREQUEST) on the server.
old-location: ldap\ldap_create_vlv_control.htm
tech.root: ldap
ms.assetid: f4305aa9-e967-45a8-8b8b-49b1e60994e8
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_create_vlv_control, ldap.ldap__create__vlv__control, ldap.ldap_create_vlv_control, ldap_create_vlv_control, ldap_create_vlv_control function [LDAP], ldap_create_vlv_controlA, ldap_create_vlv_controlW, winldap/ldap_create_vlv_control, winldap/ldap_create_vlv_controlA, winldap/ldap_create_vlv_controlW
f1_keywords:
- winldap/ldap_create_vlv_control
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
req.unicode-ansi: ldap_create_vlv_controlW (Unicode) and ldap_create_vlv_controlA (ANSI)
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
- ldap_create_vlv_control
- ldap_create_vlv_controlA
- ldap_create_vlv_controlW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_create_vlv_controlA function


## -description


The <b>ldap_create_vlv_control</b> function is used to create the request control (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-control-vlvrequest">LDAP_CONTROL_VLVREQUEST</a>) on the server.


## -parameters




### -param ExternalHandle [in]

An LDAP session handle, as obtained from a call to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_init">ldap_init</a>.


### -param VlvInfo [in]

The address of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapvlvinfo">LDAPVLVInfo</a> structure whose contents are used to construct the value of the control created.


### -param IsCritical [in]

If this value is not zero, the control created will have its criticality set to <b>TRUE</b>.


### -param Control [out]

A result parameter assigned the address of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structure that contains the request control (<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-control-vlvrequest">LDAP_CONTROL_VLVREQUEST</a>) created by this function.


## -returns



The <b>ldap_create_vlv_control</b> function returns an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">LDAP error code</a> to indicate failure, or LDAP_SUCCESS if successful.




## -remarks



When a VLV search is conducted, the client must use this function to create a new VLV control that can be included in the search request sent to the server. The server will assign a contextID for this VLV search, passed to the client. When the VLV search is completed, you should use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_control_free">ldap_control_free</a> to free the control returned by <b>ldap_create_vlv_control</b>, and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_controls_free">ldap_controls_free</a> to free the  array of controls, including the VLV response control, returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>.

For more information, and  a code example for this function, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/example-code-for-using-ldap-vlv">Example Code for Using LDAP VLV</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapvlvinfo">LDAPVLVInfo</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-control-vlvrequest">LDAP_CONTROL_VLVREQUEST</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control">Searching with the LDAP VLV Control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_vlv_controla">ldap_parse_vlv_control</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>
 

 

