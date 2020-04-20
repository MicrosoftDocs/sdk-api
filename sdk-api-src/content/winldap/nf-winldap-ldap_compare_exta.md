---
UID: NF:winldap.ldap_compare_extA
title: ldap_compare_extA function (winldap.h)
description: Use the ldap_compare_ext function to determine if an attribute, for a given entry, holds a known value.helpviewer_keywords: ["_ldap_ldap_compare_ext","ldap.ldap__compare__ext","ldap.ldap_compare_ext","ldap_compare_ext","ldap_compare_ext function [LDAP]","ldap_compare_extA","ldap_compare_extW","winldap/ldap_compare_ext","winldap/ldap_compare_extA","winldap/ldap_compare_extW"]
old-location: ldap\ldap_compare_ext.htm
tech.root: ldap
ms.assetid: 07e96a95-439b-4bb1-a9ca-d76d181e8bea
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_compare_ext, ldap.ldap__compare__ext, ldap.ldap_compare_ext, ldap_compare_ext, ldap_compare_ext function [LDAP], ldap_compare_extA, ldap_compare_extW, winldap/ldap_compare_ext, winldap/ldap_compare_extA, winldap/ldap_compare_extW
f1_keywords:
- winldap/ldap_compare_ext
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
req.unicode-ansi: ldap_compare_extW (Unicode) and ldap_compare_extA (ANSI)
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
- ldap_compare_ext
- ldap_compare_extA
- ldap_compare_extW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ldap_compare_extA function


## -description


Use the <b>ldap_compare_ext</b> function to determine if an attribute, for a given entry, holds a known value.


## -parameters




### -param ld [in]

The session handle.


### -param dn [in]

A pointer to a null-terminated string that contains the distinguished name of the entry to compare.


### -param Attr [in]

A pointer to a null-terminated string that contains the attribute to compare.


### -param Value [in]

A pointer to a null-terminated string that contains the string attribute value to be compared to the attribute value.


### -param Data [in]

The 
<a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> attribute value to be compared to the attribute value.


### -param ServerControls [in]

Optional. A list of LDAP server controls. This parameter should be set to <b>NULL</b> if not used.


### -param ClientControls [in]

Optional. A list of client controls. This parameter should be set to <b>NULL</b> if not used.


### -param MessageNumber [out]

The message ID for the compare operation.


## -returns



If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a> for more information.




## -remarks



The <b>ldap_compare_ext</b> function initiates an asynchronous compare operation, comparing the value of an attribute to a known value. The parameters and effects of <b>ldap_compare_ext</b> subsume those of 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a>. The extended routine includes additional parameters to support client and server controls, comparison of binary values, and thread safety.

Use the <i>Value</i> parameter for comparing string values or use the <i>Data</i> parameter for comparing raw binary data. Set the unused parameter to <b>NULL</b>. If neither parameter is <b>NULL</b>, the compare operation will use the value in the <i>Data</i> parameter.

If successful, <b>ldap_compare_ext</b> passes back the message ID for the operation in the <i>MessageNumber</i> parameter. Call 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to obtain the result of the compare. To have the function return the compare result directly, use the synchronous extended compare function 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>.

Multithreading: Calls to <b>ldap_compare_ext</b> are thread-safe.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/extended-controls">Extended Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/ldap/using-controls">Using Controls</a>



<a href="https://docs.microsoft.com/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare">ldap_compare</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_compare_ext_s">ldap_compare_ext_s</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>
 

 

