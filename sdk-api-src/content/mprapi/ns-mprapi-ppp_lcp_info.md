---
UID: NS:mprapi._PPP_LCP_INFO
title: PPP_LCP_INFO (mprapi.h)
description: The PPP_LCP_INFO structure contains information that describes the results of a PPP Link Control Protocol (LCP) negotiation.
helpviewer_keywords: ["PPP_LCP_CHAP","PPP_LCP_CHAP_MD5","PPP_LCP_CHAP_MS","PPP_LCP_CHAP_MSV2","PPP_LCP_EAP","PPP_LCP_INFO","PPP_LCP_INFO structure [RAS]","PPP_LCP_MULTILINK_FRAMING","PPP_LCP_PAP","PPP_LCP_SPAP","RASLCPO_3_DES","RASLCPO_ACFC","RASLCPO_DES_56","RASLCPO_PFC","RASLCPO_SSHF","_mpr_ppp_lcp_info","mprapi/PPP_LCP_INFO","rras.ppp_lcp_info"]
old-location: rras\ppp_lcp_info.htm
tech.root: RRAS
ms.assetid: b6158047-6337-483f-9a90-74d578831772
ms.date: 12/05/2018
ms.keywords: PPP_LCP_CHAP, PPP_LCP_CHAP_MD5, PPP_LCP_CHAP_MS, PPP_LCP_CHAP_MSV2, PPP_LCP_EAP, PPP_LCP_INFO, PPP_LCP_INFO structure [RAS], PPP_LCP_MULTILINK_FRAMING, PPP_LCP_PAP, PPP_LCP_SPAP, RASLCPO_3_DES, RASLCPO_ACFC, RASLCPO_DES_56, RASLCPO_PFC, RASLCPO_SSHF, _mpr_ppp_lcp_info, mprapi/PPP_LCP_INFO, rras.ppp_lcp_info
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: PPP_LCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_LCP_INFO
 - mprapi/_PPP_LCP_INFO
 - PPP_LCP_INFO
 - mprapi/PPP_LCP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_LCP_INFO
---

# PPP_LCP_INFO structure


## -description

The 
<b>PPP_LCP_INFO</b> structure contains information that describes the results of a PPP Link Control Protocol (LCP) negotiation.

## -struct-fields

### -field dwError

Specifies the error that occurred if the negotiation was unsuccessful.

### -field dwAuthenticationProtocol

Specifies the authentication protocol used to authenticate the local computer. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_PAP"></a><a id="ppp_lcp_pap"></a><dl>
<dt><b>PPP_LCP_PAP</b></dt>
</dl>
</td>
<td width="60%">
Password Authentication Protocol

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_SPAP"></a><a id="ppp_lcp_spap"></a><dl>
<dt><b>PPP_LCP_SPAP</b></dt>
</dl>
</td>
<td width="60%">
Shiva Password Authentication Protocol

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP"></a><a id="ppp_lcp_chap"></a><dl>
<dt><b>PPP_LCP_CHAP</b></dt>
</dl>
</td>
<td width="60%">
Challenge Handshake Authentication Protocol

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_EAP"></a><a id="ppp_lcp_eap"></a><dl>
<dt><b>PPP_LCP_EAP</b></dt>
</dl>
</td>
<td width="60%">
Extensible Authentication Protocol

</td>
</tr>
</table>

### -field dwAuthenticationData

Specifies additional information about the authentication protocol specified by the <b>dwAuthenticationProtocol</b> member. This member can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MD5"></a><a id="ppp_lcp_chap_md5"></a><dl>
<dt><b>PPP_LCP_CHAP_MD5</b></dt>
</dl>
</td>
<td width="60%">
MD5 CHAP

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MS"></a><a id="ppp_lcp_chap_ms"></a><dl>
<dt><b>PPP_LCP_CHAP_MS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_CHAP_MSV2"></a><a id="ppp_lcp_chap_msv2"></a><dl>
<dt><b>PPP_LCP_CHAP_MSV2</b></dt>
</dl>
</td>
<td width="60%">
Microsoft CHAP version 2

</td>
</tr>
</table>

### -field dwRemoteAuthenticationProtocol

Specifies the authentication protocol used to authenticate the remote computer. See the <b>dwAuthenticationProtocol</b> member for a list of possible values.

### -field dwRemoteAuthenticationData

Specifies additional information about the authentication protocol specified by <b>dwRemoteAuthenticationProtocol</b>. See the <b>dwAuthenticationData</b> member for a list of possible values.

### -field dwTerminateReason

Specifies the reason the connection was terminated by the local computer. This member always has a value of zero.

### -field dwRemoteTerminateReason

Specifies the reason the connection was terminated by the remote computer. This member always has a value of zero.

### -field dwOptions

Specifies information about LCP options in use by the local computer. This member is a combination of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_MULTILINK_FRAMING"></a><a id="ppp_lcp_multilink_framing"></a><dl>
<dt><b>PPP_LCP_MULTILINK_FRAMING</b></dt>
</dl>
</td>
<td width="60%">
The connection is using multilink

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_PFC"></a><a id="raslcpo_pfc"></a><dl>
<dt><b>RASLCPO_PFC</b></dt>
</dl>
</td>
<td width="60%">
Protocol Field Compression (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1172</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_ACFC"></a><a id="raslcpo_acfc"></a><dl>
<dt><b>RASLCPO_ACFC</b></dt>
</dl>
</td>
<td width="60%">
Address and Control Field Compression (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1172</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_SSHF"></a><a id="raslcpo_sshf"></a><dl>
<dt><b>RASLCPO_SSHF</b></dt>
</dl>
</td>
<td width="60%">
Short Sequence Number Header Format (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1990</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_DES_56"></a><a id="raslcpo_des_56"></a><dl>
<dt><b>RASLCPO_DES_56</b></dt>
</dl>
</td>
<td width="60%">
DES 56-bit encryption

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_3_DES"></a><a id="raslcpo_3_des"></a><dl>
<dt><b>RASLCPO_3_DES</b></dt>
</dl>
</td>
<td width="60%">
Triple DES Encryption

</td>
</tr>
</table>

### -field dwRemoteOptions

Specifies information about LCP options in use by the remote computer. This member is a combination of the following flags. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_LCP_MULTILINK_FRAMING"></a><a id="ppp_lcp_multilink_framing"></a><dl>
<dt><b>PPP_LCP_MULTILINK_FRAMING</b></dt>
</dl>
</td>
<td width="60%">
The connection is using multilink.

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_PFC"></a><a id="raslcpo_pfc"></a><dl>
<dt><b>RASLCPO_PFC</b></dt>
</dl>
</td>
<td width="60%">
Protocol Field Compression (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1172</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_ACFC"></a><a id="raslcpo_acfc"></a><dl>
<dt><b>RASLCPO_ACFC</b></dt>
</dl>
</td>
<td width="60%">
Address and Control Field Compression (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1172</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_SSHF"></a><a id="raslcpo_sshf"></a><dl>
<dt><b>RASLCPO_SSHF</b></dt>
</dl>
</td>
<td width="60%">
Short Sequence Number Header Format (see 
<a href="/windows/desktop/RRAS/remote-access-request-for-comments">RFC 1990</a>)

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_DES_56"></a><a id="raslcpo_des_56"></a><dl>
<dt><b>RASLCPO_DES_56</b></dt>
</dl>
</td>
<td width="60%">
DES 56-bit encryption

</td>
</tr>
<tr>
<td width="40%"><a id="RASLCPO_3_DES"></a><a id="raslcpo_3_des"></a><dl>
<dt><b>RASLCPO_3_DES</b></dt>
</dl>
</td>
<td width="60%">
Triple DES Encryption

</td>
</tr>
</table>

### -field dwEapTypeId

Specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the local computer. The value of this member is valid only if <b>dwAuthenticationProtocol</b> is PPP_LCP_EAP.

### -field dwRemoteEapTypeId

Specifies the type identifier of the Extensible Authentication Protocol (EAP) used to authenticate the remote computer. The value of this member is valid only if <b>dwRemoteAuthenticationProtocol</b> is PPP_LCP_EAP.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_ccp_info">PPP_CCP_INFO</a>