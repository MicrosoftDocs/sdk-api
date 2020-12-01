---
UID: NF:winldap.ldap_close_extended_op
title: ldap_close_extended_op function (winldap.h)
description: The ldap_close_extended_op function ends a request that was made by calling ldap_extended_operation.
helpviewer_keywords: ["_ldap_ldap_close_extended_op","ldap.ldap__close__extended__op","ldap.ldap_close_extended_op","ldap_close_extended_op","ldap_close_extended_op function [LDAP]","winldap/ldap_close_extended_op"]
old-location: ldap\ldap_close_extended_op.htm
tech.root: ldap
ms.assetid: 829ffb8f-150b-438a-bcbd-42f2e9c01479
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_close_extended_op, ldap.ldap__close__extended__op, ldap.ldap_close_extended_op, ldap_close_extended_op, ldap_close_extended_op function [LDAP], winldap/ldap_close_extended_op
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
 - ldap_close_extended_op
 - winldap/ldap_close_extended_op
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
 - ldap_close_extended_op
---

# ldap_close_extended_op function


## -description

The <b>ldap_close_extended_op</b> function ends a request that was made by calling 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_extended_operation">ldap_extended_operation</a>.

## -parameters

### -param ld [in]

The session handle.

### -param MessageNumber [in]

The message ID for the request.

## -returns

If the function succeeds, the return value is <b>LDAP_SUCCESS</b>.

If the function fails, it returns an error code. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

After sending an extended request, or a series of such requests, to an LDAP server, call <b>ldap_close_extended_op</b> to notify the server that the client has finished making requests. Be aware that these extended operation functions are available only with LDAP, version 3 or later. These functions allow a client to send a "free-for-all" request, for any sort of data or action, to an LDAP 3 server.

Multithreading: Calls to <b>ldap_close_extended_op</b> are thread-safe.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_extended_operation">ldap_extended_operation</a>