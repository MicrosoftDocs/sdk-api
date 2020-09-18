---
UID: NF:winber.ber_bvdup
title: ber_bvdup function (winber.h)
description: The ber_bvdup function creates a copy of the supplied berval structure.
helpviewer_keywords: ["_ldap_ber_bvdup","ber_bvdup","ber_bvdup function [LDAP]","ldap.ber__bvdup","ldap.ber_bvdup","winber/ber_bvdup"]
old-location: ldap\ber_bvdup.htm
tech.root: ldap
ms.assetid: 512addea-2738-4063-970a-10c5c365fc7d
ms.date: 12/05/2018
ms.keywords: _ldap_ber_bvdup, ber_bvdup, ber_bvdup function [LDAP], ldap.ber__bvdup, ldap.ber_bvdup, winber/ber_bvdup
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
 - ber_bvdup
 - winber/ber_bvdup
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
 - ber_bvdup
---

# ber_bvdup function


## -description

The <b>ber_bvdup</b> function creates a copy of the supplied 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

## -parameters

### -param pBerVal [in]

Pointer to the source <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

## -returns

If the function succeeds, the return value is a pointer to the newly allocated <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

If the function fails, it returns a <b>NULL</b> pointer.

## -remarks

The allocated <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> should be freed with <a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_bvfree">ber_bvfree</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>