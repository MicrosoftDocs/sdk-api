---
UID: NF:winldap.ber_bvfree
title: ber_bvfree function (winldap.h)
description: The ber_bvfree function (winldap.h) frees a berval structure, which represents arbitrary binary data that is encoded according to Basic Encoding Rules (BER).
helpviewer_keywords: ["_ldap_ber_bvfree","ber_bvfree","ber_bvfree function [LDAP]","ldap.ber__bvfree","ldap.ber_bvfree","winber/ber_bvfree","winldap/ber_bvfree"]
old-location: ldap\ber_bvfree.htm
tech.root: ldap
ms.assetid: 9e5a4bb9-568d-48ee-be75-952916c021b1
ms.date: 08/08/2022
ms.keywords: _ldap_ber_bvfree, ber_bvfree, ber_bvfree function [LDAP], ldap.ber__bvfree, ldap.ber_bvfree, winber/ber_bvfree, winldap/ber_bvfree
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
 - ber_bvfree
 - winldap/ber_bvfree
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
 - ber_bvfree
---

# ber_bvfree function


## -description

The <b>ber_bvfree</b> function frees a 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

## -parameters

### -param bv

TBD




#### - pBerVal [in]

Pointer to the <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure to be deallocated.

## -returns

None.

## -remarks

Applications should not call this function to free <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structures that they themselves have allocated.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>
