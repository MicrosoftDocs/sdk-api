---
UID: NF:winber.ber_flatten
title: ber_flatten function (winber.h)
description: The ber_flatten function allocates a new berval structure containing the data taken from the supplied BerElement structure.
helpviewer_keywords: ["_ldap_ber_flatten","ber_flatten","ber_flatten function [LDAP]","ldap.ber__flatten","ldap.ber_flatten","winber/ber_flatten"]
old-location: ldap\ber_flatten.htm
tech.root: ldap
ms.assetid: c253100b-092e-4975-8411-31edb7791068
ms.date: 12/05/2018
ms.keywords: _ldap_ber_flatten, ber_flatten, ber_flatten function [LDAP], ldap.ber__flatten, ldap.ber_flatten, winber/ber_flatten
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
 - ber_flatten
 - winber/ber_flatten
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
 - ber_flatten
---

# ber_flatten function


## -description

The <b>ber_flatten</b> function allocates a new 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure containing the data taken from the supplied 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

## -parameters

### -param pBerElement [in]

Pointer to the source <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param pBerVal [out]

Pointer to the newly allocated <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure, which should be freed using 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_bvfree">ber_bvfree</a>.

## -returns

The function returns 0 on success and -1 on failure.

## -remarks

The use of <b>ber_flatten</b> on a <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> in which all <b>{</b> and <b>}</b> format modifiers have not been properly matched will cause the function to return an error.

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_bvfree">ber_bvfree</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_init">ber_init</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>