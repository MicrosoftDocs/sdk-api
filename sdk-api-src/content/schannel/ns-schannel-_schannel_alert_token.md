---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SCHANNEL_ALERT_TOKEN structure


## -description


Generates a <a href="https://msdn.microsoft.com/45536902-af80-4dca-b3ce-207086844763">Secure Sockets Layer Protocol</a> (SSL) or Transport Layer Security Protocol (TLS) alert to be sent to the target of a call to either the <a href="https://msdn.microsoft.com/c451089a-d10d-469c-99dd-43d75a6b0b2a">InitializeSecurityContext (Schannel)</a> function or the <a href="https://msdn.microsoft.com/03fd5272-8476-4c93-8590-0d00acf6a130">AcceptSecurityContext (Schannel)</a>  function.


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

One of the alert messages defined by the TLS protocol specification. For descriptions of the defined messages, see  <a href="http://go.microsoft.com/fwlink/p/?linkid=185502">RFC 5246</a>,  <a href="http://go.microsoft.com/fwlink/p/?linkid=185503">RFC 4346</a>, or  <a href="http://go.microsoft.com/fwlink/p/?linkid=185504">RFC 2246</a>. This member must be one of the following values.



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



Add an alert message to a client context by using this structure as the value of the <i>pInput</i> parameter in a call to the <a href="https://msdn.microsoft.com/5ce13a05-874c-4e1a-9be8-aed98609791e">ApplyControlToken</a> function.



