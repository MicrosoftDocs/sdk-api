---
UID: NS:schannel._SCHANNEL_ALERT_TOKEN
title: SCHANNEL_ALERT_TOKEN (schannel.h)
description: Generates a Secure Sockets Layer Protocol (SSL) or Transport Layer Security Protocol (TLS) alert to be sent to the target of a call to either the InitializeSecurityContext (Schannel) function or the AcceptSecurityContext (Schannel) function.
helpviewer_keywords: ["SCHANNEL_ALERT_TOKEN","SCHANNEL_ALERT_TOKEN structure [Security]","TLS1_ALERT_ACCESS_DENIED","TLS1_ALERT_BAD_CERTIFICATE","TLS1_ALERT_BAD_RECORD_MAC","TLS1_ALERT_CERTIFICATE_EXPIRED","TLS1_ALERT_CERTIFICATE_REVOKED","TLS1_ALERT_CERTIFICATE_UNKNOWN","TLS1_ALERT_CLOSE_NOTIFY","TLS1_ALERT_DECODE_ERROR","TLS1_ALERT_DECOMPRESSION_FAIL","TLS1_ALERT_DECRYPTION_FAILED","TLS1_ALERT_DECRYPT_ERROR","TLS1_ALERT_EXPORT_RESTRICTION","TLS1_ALERT_FATAL","TLS1_ALERT_HANDSHAKE_FAILURE","TLS1_ALERT_ILLEGAL_PARAMETER","TLS1_ALERT_INSUFFIENT_SECURITY","TLS1_ALERT_INTERNAL_ERROR","TLS1_ALERT_NO_RENEGOTIATION","TLS1_ALERT_PROTOCOL_VERSION","TLS1_ALERT_RECORD_OVERFLOW","TLS1_ALERT_UNEXPECTED_MESSAGE","TLS1_ALERT_UNKNOWN_CA","TLS1_ALERT_UNSUPPORTED_CERT","TLS1_ALERT_UNSUPPORTED_EXT","TLS1_ALERT_USER_CANCELED","TLS1_ALERT_WARNING","schannel/SCHANNEL_ALERT_TOKEN","security.schannel_alert_token"]
old-location: security\schannel_alert_token.htm
tech.root: security
ms.assetid: 1c3a896d-4252-44ef-9e4b-6ad00e3d6f05
ms.date: 12/05/2018
ms.keywords: SCHANNEL_ALERT_TOKEN, SCHANNEL_ALERT_TOKEN structure [Security], TLS1_ALERT_ACCESS_DENIED, TLS1_ALERT_BAD_CERTIFICATE, TLS1_ALERT_BAD_RECORD_MAC, TLS1_ALERT_CERTIFICATE_EXPIRED, TLS1_ALERT_CERTIFICATE_REVOKED, TLS1_ALERT_CERTIFICATE_UNKNOWN, TLS1_ALERT_CLOSE_NOTIFY, TLS1_ALERT_DECODE_ERROR, TLS1_ALERT_DECOMPRESSION_FAIL, TLS1_ALERT_DECRYPTION_FAILED, TLS1_ALERT_DECRYPT_ERROR, TLS1_ALERT_EXPORT_RESTRICTION, TLS1_ALERT_FATAL, TLS1_ALERT_HANDSHAKE_FAILURE, TLS1_ALERT_ILLEGAL_PARAMETER, TLS1_ALERT_INSUFFIENT_SECURITY, TLS1_ALERT_INTERNAL_ERROR, TLS1_ALERT_NO_RENEGOTIATION, TLS1_ALERT_PROTOCOL_VERSION, TLS1_ALERT_RECORD_OVERFLOW, TLS1_ALERT_UNEXPECTED_MESSAGE, TLS1_ALERT_UNKNOWN_CA, TLS1_ALERT_UNSUPPORTED_CERT, TLS1_ALERT_UNSUPPORTED_EXT, TLS1_ALERT_USER_CANCELED, TLS1_ALERT_WARNING, schannel/SCHANNEL_ALERT_TOKEN, security.schannel_alert_token
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCHANNEL_ALERT_TOKEN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCHANNEL_ALERT_TOKEN
 - schannel/_SCHANNEL_ALERT_TOKEN
 - SCHANNEL_ALERT_TOKEN
 - schannel/SCHANNEL_ALERT_TOKEN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Schannel.h
api_name:
 - SCHANNEL_ALERT_TOKEN
---

# SCHANNEL_ALERT_TOKEN structure


## -description

Generates a <a href="/windows/desktop/SecAuthN/secure-sockets-layer-protocol">Secure Sockets Layer Protocol</a> (SSL) or Transport Layer Security Protocol (TLS) alert to be sent to the target of a call to either the <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">InitializeSecurityContext (Schannel)</a> function or the <a href="/windows/desktop/api/sspi/nf-sspi-acceptsecuritycontext">AcceptSecurityContext (Schannel)</a>  function.

## -struct-fields

### -field dwTokenType

Specifies the type of this structure. Set the value of this member to <b>SCHANNEL_ALERT</b>.

### -field dwAlertType

Specifies the alert type. This must be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TLS1_ALERT_WARNING"></a><a id="tls1_alert_warning"></a><dl>
<dt><b>TLS1_ALERT_WARNING</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The message is a warning.

</td>
</tr>
<tr>
<td width="40%"><a id="TLS1_ALERT_FATAL"></a><a id="tls1_alert_fatal"></a><dl>
<dt><b>TLS1_ALERT_FATAL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The message is a fatal error. The connection is closed immediately.

</td>
</tr>
</table>

### -field dwAlertNumber

One of the alert messages defined by the TLS protocol specification. For descriptions of the defined messages, see  <a href="http://tools.ietf.org/html/rfc5246#section-7.2">RFC 5246</a>,  <a href="http://tools.ietf.org/html/rfc4346#section-7.2">RFC 4346</a>, or  <a href="http://tools.ietf.org/html/rfc2246#section-7.2">RFC 2246</a>. This member must be one of the following values.



#### TLS1_ALERT_CLOSE_NOTIFY (0)



#### TLS1_ALERT_UNEXPECTED_MESSAGE (10)



#### TLS1_ALERT_BAD_RECORD_MAC (20)



#### TLS1_ALERT_DECRYPTION_FAILED (21)



#### TLS1_ALERT_RECORD_OVERFLOW (22)



#### TLS1_ALERT_DECOMPRESSION_FAIL (30)



#### TLS1_ALERT_HANDSHAKE_FAILURE (40)



#### TLS1_ALERT_BAD_CERTIFICATE (42)



#### TLS1_ALERT_UNSUPPORTED_CERT (43)



#### TLS1_ALERT_CERTIFICATE_REVOKED (44)



#### TLS1_ALERT_CERTIFICATE_EXPIRED (45)



#### TLS1_ALERT_CERTIFICATE_UNKNOWN (46)



#### TLS1_ALERT_ILLEGAL_PARAMETER (47)



#### TLS1_ALERT_UNKNOWN_CA (48)



#### TLS1_ALERT_ACCESS_DENIED (49)



#### TLS1_ALERT_DECODE_ERROR (50)



#### TLS1_ALERT_DECRYPT_ERROR (51)



#### TLS1_ALERT_EXPORT_RESTRICTION (60)



#### TLS1_ALERT_PROTOCOL_VERSION (70)



#### TLS1_ALERT_INSUFFIENT_SECURITY (71)



#### TLS1_ALERT_INTERNAL_ERROR (80)



#### TLS1_ALERT_USER_CANCELED (90)



#### TLS1_ALERT_NO_RENEGOTIATION (100)



#### TLS1_ALERT_UNSUPPORTED_EXT (110)

## -remarks

Add an alert message to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="/windows/desktop/api/sspi/nf-sspi-applycontroltoken">ApplyControlToken</a> function.