---
UID: NF:winber.ber_init
title: ber_init function (winber.h)
description: The ber_init function allocates a new BerElement structure containing the data taken from the supplied berval structure.
helpviewer_keywords: ["_ldap_ber_init","ber_init","ber_init function [LDAP]","ldap.ber__init","ldap.ber_init","winber/ber_init"]
old-location: ldap\ber_init.htm
tech.root: ldap
ms.assetid: ad6557e9-1683-4ffd-a59e-8f37eb67d089
ms.date: 12/05/2018
ms.keywords: _ldap_ber_init, ber_init, ber_init function [LDAP], ldap.ber__init, ldap.ber_init, winber/ber_init
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
 - ber_init
 - winber/ber_init
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
 - ber_init
---

# ber_init function


## -description

The <b>ber_init</b> function allocates a new 
<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure containing the data taken from the supplied 
<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

## -parameters

### -param pBerVal [in]

Pointer to the source <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a> structure.

## -returns

If the function succeeds, the return value is a pointer to the newly allocated <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

If the function fails, it returns a <b>NULL</b> pointer.

## -remarks

Call 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a> to free a <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure allocated with this function.

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_free">ber_free</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>