---
UID: NF:winldap.ldap_result2error
title: ldap_result2error function (winldap.h)
description: The ldap_result2error function parses a message and returns the error code.
helpviewer_keywords: ["_ldap_ldap_result2error","ldap.ldap__result2error","ldap.ldap_result2error","ldap_result2error","ldap_result2error function [LDAP]","winldap/ldap_result2error"]
old-location: ldap\ldap_result2error.htm
tech.root: ldap
ms.assetid: 67198ed0-c210-4eb1-b0f9-13cdb128c57d
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_result2error, ldap.ldap__result2error, ldap.ldap_result2error, ldap_result2error, ldap_result2error function [LDAP], winldap/ldap_result2error
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
 - ldap_result2error
 - winldap/ldap_result2error
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
 - ldap_result2error
---

# ldap_result2error function


## -description

The <b>ldap_result2error</b> function parses a message and returns the error code.

## -parameters

### -param ld [in]

The session handle.

### -param res [in]

The result of an LDAP operation, as returned by 

<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>, or one of the synchronous API operation calls.

### -param freeit [in]

Determines whether the <a href="/windows/win32/api/winldap/ns-winldap-ldapmessage">LDAPMessage</a>, pointed to by the <i>res</i> parameter, is freed. Setting <i>freeit</i> to <b>TRUE</b> frees the message by calling the 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a> function.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 

<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

Multithreading: Calls to <b>ldap_result2error</b> are thread-safe.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>

