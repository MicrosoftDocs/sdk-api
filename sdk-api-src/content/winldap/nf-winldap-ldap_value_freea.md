---
UID: NF:winldap.ldap_value_freeA
title: ldap_value_freeA function (winldap.h)
description: Frees a structure returned by ldap_get_values. (ldap_value_freeA)
helpviewer_keywords: ["ldap.ldap__value__free", "ldap_value_freeA", "winldap/ldap_value_freeA"]
old-location: ldap\ldap_value_free.htm
tech.root: ldap
ms.assetid: 67c9f04c-4b8e-4e97-902d-fceccf27f522
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_value_free, ldap.ldap__value__free, ldap.ldap_value_free, ldap_value_free, ldap_value_free function [LDAP], ldap_value_freeA, ldap_value_freeW, winldap/ldap_value_free, winldap/ldap_value_freeA, winldap/ldap_value_freeW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_value_freeW (Unicode) and ldap_value_freeA (ANSI)
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
 - ldap_value_freeA
 - winldap/ldap_value_freeA
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
 - ldap_value_free
 - ldap_value_freeA
 - ldap_value_freeW
---

# ldap_value_freeA function


## -description

The <b>ldap_value_free</b> function frees a structure returned by 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>.

## -parameters

### -param vals

The structure to free.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see <a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Call <b>ldap_value_free</b> to free a structure returned by <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/searching-a-directory">Searching a Directory</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_get_values">ldap_get_values</a>
