---
UID: NF:winber.ber_bvecfree
title: ber_bvecfree function (winber.h)
description: The ber_bvecfree function frees an array of berval structures.
helpviewer_keywords: ["_ldap_ber_bvecfree","ber_bvecfree","ber_bvecfree function [LDAP]","ldap.ber__bvecfree","ldap.ber_bvecfree","winber/ber_bvecfree"]
old-location: ldap\ber_bvecfree.htm
tech.root: ldap
ms.assetid: 5c2b53e4-257e-4c3f-b712-345e6b33341b
ms.date: 12/05/2018
ms.keywords: _ldap_ber_bvecfree, ber_bvecfree, ber_bvecfree function [LDAP], ldap.ber__bvecfree, ldap.ber_bvecfree, winber/ber_bvecfree
req.header: winber.h
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
 - ber_bvecfree
 - winber/ber_bvecfree
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
 - ber_bvecfree
---

# ber_bvecfree function


## -description

The <b>ber_bvecfree</b> function frees an array of 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures.

## -parameters

### -param pBerVal [in]

Pointer to a NULL-terminated array of <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures to be deallocated.

## -returns

None.

## -remarks

Use this function only to free an array of 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures returned by <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_scanf">ber_scanf</a> with the <b>V</b> character included in the format string.

An application should not call this function to free a <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures that it has allocated.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>