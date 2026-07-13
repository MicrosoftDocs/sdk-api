---
UID: NF:winldap.ldap_parse_vlv_controlW
title: ldap_parse_vlv_controlW function (winldap.h)
description: Used to find and parse VLV search results. (Unicode)
helpviewer_keywords: ["_ldap_ldap_parse_vlv_control", "ldap.ldap__parse__vlv__control", "ldap.ldap_parse_vlv_control", "ldap_parse_vlv_control", "ldap_parse_vlv_control function [LDAP]", "ldap_parse_vlv_controlW", "winldap/ldap_parse_vlv_control", "winldap/ldap_parse_vlv_controlW"]
old-location: ldap\ldap_parse_vlv_control.htm
tech.root: ldap
ms.assetid: a1a1e47f-c53b-48a3-9c40-0e1518c5c729
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_parse_vlv_control, ldap.ldap__parse__vlv__control, ldap.ldap_parse_vlv_control, ldap_parse_vlv_control, ldap_parse_vlv_control function [LDAP], ldap_parse_vlv_controlA, ldap_parse_vlv_controlW, winldap/ldap_parse_vlv_control, winldap/ldap_parse_vlv_controlA, winldap/ldap_parse_vlv_controlW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_parse_vlv_controlW (Unicode) and ldap_parse_vlv_controlA (ANSI)
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
 - ldap_parse_vlv_controlW
 - winldap/ldap_parse_vlv_controlW
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
 - ldap_parse_vlv_control
 - ldap_parse_vlv_controlA
 - ldap_parse_vlv_controlW
---

# ldap_parse_vlv_controlW function


## -description

The <b>ldap_parse_vlv_control</b> function is used to find and parse VLV search results.

## -parameters

### -param ExternalHandle [in]

The LDAP session handle.

### -param Control [in]

The address of a NULL-terminated array of <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a> structures, typically obtained by a call to 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_parse_result">ldap_parse_result</a>.

### -param TargetPos [out]

The numeric position of the target entry in the result set list, as provided by the targetPosition element of the BER-encoded response control (<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the target position is not returned.

### -param ListCount [out]

The server estimate of the number of entries in the list as provided by the contentCount element of the BER-encoded response control (<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the size is not returned.

### -param Context [out]

The server-generated context identifier. If the server does not return a context identifier, this parameter will be set to <b>NULL</b>. If <b>NULL</b> is passed for contextp, the context identifier is not returned.

### -param ErrCode [out]

The VLV result code, as provided by the virtualListViewResult element of the BER-encoded response control (<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>). If this parameter is <b>NULL</b>, the result code is not returned.

## -returns

This function returns an 
<a href="/previous-versions/windows/desktop/ldap/return-values">LDAP error code</a> that indicates whether a VLV result control was found and parsed successfully. <b>LDAP_SUCCESS</b> is returned if all goes well, <b>LDAP_CONTROL_MISSING</b> is returned if the <i>ctrls</i> array does not include a response control (<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>), and another LDAP error code is returned if a parsing error or other issue occurs.

VLV uses the following LDAP return value codes:

<b>LDAP_OPERATIONS_ERROR</b>

<b>LDAP_UNWILLING_TO_PERFORM</b>

<b>LDAP_INSUFFICIENT_ACCESS</b>

<b>LDAP_BUSY</b>

<b>LDAP_TIMELIMIT_EXCEEDED</b>

<b>LDAP_ADMINLIMIT_EXCEEDED</b>

<b>LDAP_OTHER</b>

In addition, the following two codes have been added to support VLV:

## -remarks

This control parses the search results returned by the server in the response control (<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>). A context identifier is passed from the server to the client to identify the control, which must be freed at the end of the session by calling 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_bvfree">ber_bvfree</a>.

For more information and a code example, see 
<a href="/previous-versions/windows/desktop/ldap/example-code-for-using-ldap-vlv">Example Code for Using LDAP VLV</a>.





> [!NOTE]
> The winldap.h header defines ldap_parse_vlv_control as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapcontrola">LDAPControl</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldapvlvinfo">LDAPVLVInfo</a>



<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvrequest">LDAP_CONTROL_VLVREQUEST</a>



<a href="/previous-versions/windows/desktop/ldap/ldap-control-vlvresponse">LDAP_CONTROL_VLVRESPONSE</a>



<a href="/previous-versions/windows/desktop/ldap/searching-with-the-ldap-vlv-control">Searching with the LDAP VLV Control</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_sort_control">ldap_create_sort_control</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_create_vlv_controla">ldap_create_vlv_control</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext">ldap_search_ext</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search_ext_s">ldap_search_ext_s</a>
