---
UID: NF:winldap.ldap_result
title: ldap_result function (winldap.h)
description: Obtains the result of an asynchronous operation.
helpviewer_keywords: ["_ldap_ldap_result","ldap.ldap__result","ldap.ldap_result","ldap_result","ldap_result function [LDAP]","winldap/ldap_result"]
old-location: ldap\ldap_result.htm
tech.root: ldap
ms.assetid: e047fccc-a875-4360-be1b-3ac3dea15dd6
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_result, ldap.ldap__result, ldap.ldap_result, ldap_result, ldap_result function [LDAP], winldap/ldap_result
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
 - ldap_result
 - winldap/ldap_result
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
 - ldap_result
---

# ldap_result function


## -description

The <b>ldap_result</b> function obtains the result of an asynchronous operation.

## -parameters

### -param ld [in]

The session handle.

### -param msgid [in]

The message ID of the operation, or the constant LDAP_RES_ANY if any result is required.

### -param all [in]

Specifies how many messages are retrieved in a single call to <b>ldap_result</b>. This parameter only has meaning for search results. Pass the constant LDAP_MSG_ONE (0x00) to retrieve one message at a time. Pass LDAP_MSG_ALL (0x01) to request that all results of a search be received before returning all results in a single chain. Pass LDAP_MSG_RECEIVED (0x02) to indicate that all results retrieved so far should be returned in the result chain.

### -param timeout [in]

A timeout that specifies how long, in seconds, to wait for results to be returned. A <b>NULL</b> value causes <b>ldap_result</b> to block until results are available. A timeout value of zero seconds specifies a polling behavior.

### -param res [out]

Contains the result(s) of the operation. Any results returned should be freed with a call to <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a> once they are no longer required by the application.

## -returns

If the function succeeds, it returns one of the following values to indicate the type of the first result in the <i>res</i> parameter. If the time-out expires, the function returns 0.

If the function fails, it returns –1 and sets the session error parameters in the LDAP data structure.

## -remarks

The <b>ldap_result</b> function retrieves the result of a previous, asynchronously initiated operation. Be aware that, depending on the way it is called, <b>ldap_result</b> may actually return a list or "chain" of messages.

For connectionless LDAP, you must pass both an LDAP connection handle and a message ID to ensure that you get the correct results. The LDAP run time continues to send the request until it receives a response.

Multithreading: Calls to <b>ldap_result</b> are thread safe.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_msgfree">ldap_msgfree</a>