---
UID: NF:winldap.ldap_extended_operationW
title: ldap_extended_operationW function (winldap.h)
description: The ldap_extended_operationW (Unicode) function (winldap.h) enables you to pass extended LDAP operations to the server. 
helpviewer_keywords: ["_ldap_ldap_extended_operation", "ldap.ldap__extended__operation", "ldap.ldap_extended_operation", "ldap_extended_operation", "ldap_extended_operation function [LDAP]", "ldap_extended_operationW", "winldap/ldap_extended_operation", "winldap/ldap_extended_operationW"]
old-location: ldap\ldap_extended_operation.htm
tech.root: ldap
ms.assetid: 02dda7c5-9779-4390-9395-aa917fa82546
ms.date: 08/09/2022
ms.keywords: _ldap_ldap_extended_operation, ldap.ldap__extended__operation, ldap.ldap_extended_operation, ldap_extended_operation, ldap_extended_operation function [LDAP], ldap_extended_operationA, ldap_extended_operationW, winldap/ldap_extended_operation, winldap/ldap_extended_operationA, winldap/ldap_extended_operationW
req.header: winldap.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ldap_extended_operationW (Unicode) and ldap_extended_operationA (ANSI)
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
 - ldap_extended_operationW
 - winldap/ldap_extended_operationW
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
 - ldap_extended_operation
 - ldap_extended_operationA
 - ldap_extended_operationW
---

# ldap_extended_operationW function


## -description

The <b>ldap_extended_operation</b> function enables you to pass extended LDAP operations to the server.

## -parameters

### -param ld [in]

The session handle.

### -param Oid [in]

A pointer to a null-terminated string that contains the dotted object identifier  text string that names the request.

### -param Data [in]

The arbitrary data required by the operation. If <b>NULL</b>, no data is sent to the server.

### -param ServerControls [in]

Optional. A list of LDAP server controls. Set this parameter to <b>NULL</b>, if not used.

### -param ClientControls [in]

Optional. A list of client controls. Set this parameter to <b>NULL</b>, if not used.

### -param MessageNumber [out]

The message ID for the request.

## -returns

If the function succeeds, <b>LDAP_SUCCESS</b> is returned.

If the function fails, an error code is returned. For more information, see 
<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>.

## -remarks

The <b>ldap_extended_operation</b> function enables a client to send an extended request (free for all) to an LDAP 3 (or later) server. The functionality is open and the client request can be for any operation.

As an asynchronous function, <b>ldap_extended_operation</b> returns a message ID for the operation. Call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a> with the message ID to get the result of the operation. To cancel an asynchronous operation, call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>.

Because of the open nature of the request, the client must call 
<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_close_extended_op">ldap_close_extended_op</a> to terminate the request.

Multithreading: The <b>ldap_extended_operation</b> function is thread-safe.





> [!NOTE]
> The winldap.h header defines ldap_extended_operation as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/ldap/return-values">Return Values</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_abandon">ldap_abandon</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_close_extended_op">ldap_close_extended_op</a>



<a href="/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_result">ldap_result</a>
