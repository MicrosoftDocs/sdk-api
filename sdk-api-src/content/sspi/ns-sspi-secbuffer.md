---
UID: NS:sspi._SecBuffer
title: SecBuffer (sspi.h)
description: Describes a buffer allocated by a transport application to pass to a security package.
helpviewer_keywords: ["*PSecBuffer","PSecBuffer","PSecBuffer structure pointer [Security]","SECBUFFER_ALERT","SECBUFFER_APPLICATION_PROTOCOLS","SECBUFFER_ATTRMASK","SECBUFFER_CHANGE_PASS_RESPONSE","SECBUFFER_CHANNEL_BINDINGS","SECBUFFER_DATA","SECBUFFER_DTLS_MTU","SECBUFFER_EMPTY","SECBUFFER_EXTRA","SECBUFFER_MECHLIST","SECBUFFER_MECHLIST_SIGNATURE","SECBUFFER_MISSING","SECBUFFER_PKG_PARAMS","SECBUFFER_PRESHARED_KEY","SECBUFFER_PRESHARED_KEY_IDENTITY","SECBUFFER_READONLY","SECBUFFER_READONLY_WITH_CHECKSUM","SECBUFFER_SRTP_MASTER_KEY_IDENTIFIER","SECBUFFER_SRTP_PROTECTION_PROFILES","SECBUFFER_STREAM_HEADER","SECBUFFER_STREAM_TRAILER","SECBUFFER_TARGET","SECBUFFER_TARGET_HOST","SECBUFFER_TOKEN","SECBUFFER_TOKEN_BINDING","SecBuffer","SecBuffer structure [Security]","_ssp_secbuffer","security.secbuffer","sspi/PSecBuffer","sspi/SecBuffer"]
old-location: security\secbuffer.htm
tech.root: security
ms.assetid: 75f49d9c-7d3c-4f45-a94e-44cd05773a07
ms.date: 12/05/2018
ms.keywords: '*PSecBuffer, PSecBuffer, PSecBuffer structure pointer [Security], SECBUFFER_ALERT, SECBUFFER_APPLICATION_PROTOCOLS, SECBUFFER_ATTRMASK, SECBUFFER_CHANGE_PASS_RESPONSE, SECBUFFER_CHANNEL_BINDINGS, SECBUFFER_DATA, SECBUFFER_DTLS_MTU, SECBUFFER_EMPTY, SECBUFFER_EXTRA, SECBUFFER_MECHLIST, SECBUFFER_MECHLIST_SIGNATURE, SECBUFFER_MISSING, SECBUFFER_PKG_PARAMS, SECBUFFER_PRESHARED_KEY, SECBUFFER_PRESHARED_KEY_IDENTITY, SECBUFFER_READONLY, SECBUFFER_READONLY_WITH_CHECKSUM, SECBUFFER_SRTP_MASTER_KEY_IDENTIFIER, SECBUFFER_SRTP_PROTECTION_PROFILES, SECBUFFER_STREAM_HEADER, SECBUFFER_STREAM_TRAILER, SECBUFFER_TARGET, SECBUFFER_TARGET_HOST, SECBUFFER_TOKEN, SECBUFFER_TOKEN_BINDING, SecBuffer, SecBuffer structure [Security], _ssp_secbuffer, security.secbuffer, sspi/PSecBuffer, sspi/SecBuffer'
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: SecBuffer, *PSecBuffer
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecBuffer
 - sspi/_SecBuffer
 - PSecBuffer
 - sspi/PSecBuffer
 - SecBuffer
 - sspi/SecBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Sspi.h
api_name:
 - SecBuffer
---

# SecBuffer structure


## -description

The <b>SecBuffer</b> structure describes a buffer allocated by a transport application to pass to a <a href="/windows/desktop/SecGloss/s-gly">security package</a>.

## -struct-fields

### -field cbBuffer

Specifies the size, in bytes, of the buffer pointed to by the <b>pvBuffer</b> member.

### -field BufferType

Bit flags that indicate the type of buffer. <b>BufferType</b> must be one of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_ALERT"></a><a id="secbuffer_alert"></a><dl>
<dt><b>SECBUFFER_ALERT</b></dt>
<dt>17 (0x11)</dt>
</dl>
</td>
<td width="60%">
The buffer contains an alert message.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_ATTRMASK"></a><a id="secbuffer_attrmask"></a><dl>
<dt><b>SECBUFFER_ATTRMASK</b></dt>
<dt>4026531840 (0xF0000000)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a bitmask for a SECBUFFER_READONLY_WITH_CHECKSUM buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_CHANNEL_BINDINGS"></a><a id="secbuffer_channel_bindings"></a><dl>
<dt><b>SECBUFFER_CHANNEL_BINDINGS</b></dt>
<dt>14 (0xE)</dt>
</dl>
</td>
<td width="60%">
The buffer contains channel binding information.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_CHANGE_PASS_RESPONSE"></a><a id="secbuffer_change_pass_response"></a><dl>
<dt><b>SECBUFFER_CHANGE_PASS_RESPONSE</b></dt>
<dt>15 (0xF)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a <a href="/windows/desktop/api/ntsecapi/ns-ntsecapi-domain_password_information">DOMAIN_PASSWORD_INFORMATION</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_DATA"></a><a id="secbuffer_data"></a><dl>
<dt><b>SECBUFFER_DATA</b></dt>
<dt>1 (0x1)</dt>
</dl>
</td>
<td width="60%">
The buffer contains common data. The security package can read and write this data, for example, to encrypt some or all of it.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_DTLS_MTU"></a><a id="secbuffer_dtls_mtu"></a><dl>
<dt><b>SECBUFFER_DTLS_MTU</b></dt>
<dt>24 (0x18)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the setting for the maximum transmission unit (MTU) size for DTLS only. The default value is 1096 and the valid configurable range is between 200 and 64*1024.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_EMPTY"></a><a id="secbuffer_empty"></a><dl>
<dt><b>SECBUFFER_EMPTY</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
This is a placeholder in the buffer array. The caller can supply several such entries in the array, and the security package can return information in them. For more information, see 
<a href="/windows/desktop/SecAuthN/sspi-context-semantics">SSPI Context Semantics</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_EXTRA"></a><a id="secbuffer_extra"></a><dl>
<dt><b>SECBUFFER_EXTRA</b></dt>
<dt>5 (0x5)</dt>
</dl>
</td>
<td width="60%">
The security package uses this value to indicate the number of extra or unprocessed bytes in a message.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_MECHLIST"></a><a id="secbuffer_mechlist"></a><dl>
<dt><b>SECBUFFER_MECHLIST</b></dt>
<dt>11 (0xB)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a protocol-specific list of <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs). It is not usually of interest to callers.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_MECHLIST_SIGNATURE"></a><a id="secbuffer_mechlist_signature"></a><dl>
<dt><b>SECBUFFER_MECHLIST_SIGNATURE</b></dt>
<dt>12 (0xC)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a signature of a <b>SECBUFFER_MECHLIST</b> buffer. It is not usually of interest to callers.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_MISSING"></a><a id="secbuffer_missing"></a><dl>
<dt><b>SECBUFFER_MISSING</b></dt>
<dt>4 (0x4)</dt>
</dl>
</td>
<td width="60%">
The security package uses this value to indicate the number of missing bytes in a particular message. The <b>pvBuffer</b> member is ignored in this type.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_PKG_PARAMS"></a><a id="secbuffer_pkg_params"></a><dl>
<dt><b>SECBUFFER_PKG_PARAMS</b></dt>
<dt>3 (0x3)</dt>
</dl>
</td>
<td width="60%">
These are transport-to-package–specific parameters. For example, the NetWare redirector may supply the server <a href="/windows/desktop/SecGloss/o-gly">object identifier</a>, while DCE RPC can supply an association <b>UUID</b>, and so on.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_PRESHARED_KEY"></a><a id="secbuffer_preshared_key"></a><dl>
<dt><b>SECBUFFER_PRESHARED_KEY</b></dt>
<dt>22 (0x16)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the preshared key. The maximum allowed PSK buffer size is 256 bytes. 

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_PRESHARED_KEY_IDENTITY"></a><a id="secbuffer_preshared_key_identity"></a><dl>
<dt><b>SECBUFFER_PRESHARED_KEY_IDENTITY</b></dt>
<dt>23 (0x17)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the preshared key identity.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_SRTP_MASTER_KEY_IDENTIFIER"></a><a id="secbuffer_srtp_master_key_identifier"></a><dl>
<dt><b>SECBUFFER_SRTP_MASTER_KEY_IDENTIFIER</b></dt>
<dt>20 (0x14)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the SRTP master key identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_SRTP_PROTECTION_PROFILES"></a><a id="secbuffer_srtp_protection_profiles"></a><dl>
<dt><b>SECBUFFER_SRTP_PROTECTION_PROFILES</b></dt>
<dt>19 (0x13)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the list of SRTP protection profiles, in descending order of preference.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_STREAM_HEADER"></a><a id="secbuffer_stream_header"></a><dl>
<dt><b>SECBUFFER_STREAM_HEADER</b></dt>
<dt>7 (0x7)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a protocol-specific header for a particular record. It is not usually of interest to callers.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_STREAM_TRAILER"></a><a id="secbuffer_stream_trailer"></a><dl>
<dt><b>SECBUFFER_STREAM_TRAILER</b></dt>
<dt>6 (0x6)</dt>
</dl>
</td>
<td width="60%">
The buffer contains a protocol-specific trailer for a particular record. It is not usually of interest to callers.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_TARGET"></a><a id="secbuffer_target"></a><dl>
<dt><b>SECBUFFER_TARGET</b></dt>
<dt>13 (0xD)</dt>
</dl>
</td>
<td width="60%">
This flag is reserved. Do not use it.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_TARGET_HOST"></a><a id="secbuffer_target_host"></a><dl>
<dt><b>SECBUFFER_TARGET_HOST</b></dt>
<dt>16 (0x10)</dt>
</dl>
</td>
<td width="60%">
The buffer specifies the <a href="/windows/desktop/SecGloss/s-gly">service principal name</a> (SPN) of the target.

This value is supported by the Digest security package when used with channel bindings.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_TOKEN"></a><a id="secbuffer_token"></a><dl>
<dt><b>SECBUFFER_TOKEN</b></dt>
<dt>2 (0x2)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the security token portion of the message. This is read-only for input parameters or read/write for output parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_TOKEN_BINDING"></a><a id="secbuffer_token_binding"></a><dl>
<dt><b>SECBUFFER_TOKEN_BINDING</b></dt>
<dt>21 (0x15)</dt>
</dl>
</td>
<td width="60%">
The buffer contains the supported token binding protocol version and key parameters, in descending order of preference.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_APPLICATION_PROTOCOLS"></a><a id="secbuffer_application_protocols"></a><dl>
<dt><b>SECBUFFER_APPLICATION_PROTOCOLS</b></dt>
<dt>18</dt>
</dl>
</td>
<td width="60%">
The buffer contains a list of application protocol IDs, one list per application protocol negotiation extension type to be enabled.

</td>
</tr>
</table>
 


In addition, <b>BufferType</b> can combine the following flags with any of the flags in the preceding table by using a bitwise-<b>OR</b> operation.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_READONLY"></a><a id="secbuffer_readonly"></a><dl>
<dt><b>SECBUFFER_READONLY</b></dt>
<dt>2147483648 (0x80000000)</dt>
</dl>
</td>
<td width="60%">
The buffer is read-only with no checksum. This flag is intended for sending header information to the security package for computing the checksum. The package can read this buffer, but cannot modify it.

</td>
</tr>
<tr>
<td width="40%"><a id="SECBUFFER_READONLY_WITH_CHECKSUM"></a><a id="secbuffer_readonly_with_checksum"></a><dl>
<dt><b>SECBUFFER_READONLY_WITH_CHECKSUM</b></dt>
<dt>268435456 (0x10000000)</dt>
</dl>
</td>
<td width="60%">
The buffer is read-only with a checksum.

</td>
</tr>
</table>

### -field pvBuffer.size_is

### -field pvBuffer.size_is.cbBuffer

### -field pvBuffer

A pointer to a buffer.

## -see-also

<a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a>