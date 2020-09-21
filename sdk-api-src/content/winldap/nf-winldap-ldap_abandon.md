---
UID: NF:winldap.ldap_abandon
title: ldap_abandon function (winldap.h)
description: A client calls ldap_abandon to cancel an in-process asynchronous LDAP call.
helpviewer_keywords: ["_ldap_ldap_abandon","ldap.ldap__abandon","ldap.ldap_abandon","ldap_abandon","ldap_abandon function [LDAP]","winldap/ldap_abandon"]
old-location: ldap\ldap_abandon.htm
tech.root: ldap
ms.assetid: 5c238d98-77f5-4702-bae1-80cdec70a30c
ms.date: 12/05/2018
ms.keywords: _ldap_ldap_abandon, ldap.ldap__abandon, ldap.ldap_abandon, ldap_abandon, ldap_abandon function [LDAP], winldap/ldap_abandon
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
 - ldap_abandon
 - winldap/ldap_abandon
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
 - ldap_abandon
---

# ldap_abandon function


## -description

A client calls <b>ldap_abandon</b> to cancel an in-process asynchronous LDAP call.

## -parameters

### -param ld [in]

The session handle.

### -param msgid [in]

The message ID of the call to be canceled. Asynchronous functions, such as <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_search">ldap_search</a> and <a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify">ldap_modify</a>,  return this message ID when they initiate an operation.

## -returns

If the function succeeds, that is, if the cancel operation is successful, the return value is zero.

If the function fails, the return value is –1.

## -remarks

The <b>ldap_abandon</b> function first verifies that the operation has been completed. If it has, the message ID is deleted; otherwise, the call goes to the server to cancel the operation. Be aware that a successful call to <b>ldap_abandon</b> destroys the message ID. Therefore, you cannot call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> to obtain results with that message ID, even if the server completed the operation.

There is no server response to <b>ldap_abandon</b>; thus, there is no guarantee that the call reached the server.

Multithreading: Calls to <b>ldap_abandon</b> are thread-safe.

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>