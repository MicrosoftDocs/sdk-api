---
UID: NF:winldap.ldap_count_values_len
title: ldap_count_values_len function (winldap.h)
description: Counts the number of values in a list.
helpviewer_keywords: ["_ldap_ldap_count_values_len","ldap.ldap__count__values__len","ldap.ldap_count_values_len","ldap_count_values_len","ldap_count_values_len function [LDAP]","winldap/ldap_count_values_len"]
old-location: ldap\ldap_count_values_len.htm
tech.root: ldap
ms.assetid: fab632c7-3ec6-4968-a48d-5865e7f43d0b
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_count_values_len, ldap.ldap__count__values__len, ldap.ldap_count_values_len, ldap_count_values_len, ldap_count_values_len function [LDAP], winldap/ldap_count_values_len
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - ldap_count_values_len
 - winldap/ldap_count_values_len
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
 - ldap_count_values_len
---

# ldap_count_values_len function


## -description

The <b>ldap_count_values_len</b> function counts the number of values in a list.

## -parameters

### -param vals [in]

An array of values returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>.

## -returns

This function returns the number of values in the array. There is no error return.

If a <b>NULL</b> pointer is passed as the argument, 0 is returned. If an invalid argument is passed, the value returned is undefined.

## -remarks

The <b>ldap_count_values_len</b> function returns the number of binary values in an array of 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures. To count the values in an array of null-terminated character strings, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-ldap">LDAP</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_count_values">ldap_count_values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values_len">ldap_get_values_len</a>