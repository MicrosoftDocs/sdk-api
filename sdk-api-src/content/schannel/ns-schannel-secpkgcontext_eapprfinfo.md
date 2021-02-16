---
UID: NS:schannel._SecPkgContext_EapPrfInfo
title: SecPkgContext_EapPrfInfo (schannel.h)
description: Specifies the pseudorandom function (PRF) and extracts key data used by the Extensible Authentication Protocol (EAP) Transport Layer Security protocol (TLS) Authentication Protocol.
helpviewer_keywords: ["*PSecPkgContext_EapPrfInfo","EAP-FAST Keying Material","EAP-TTLSv0 Challenge Data","EAP-TTLSv0 Keying Material","PPP EAP TLS Key Data","PSecPkgContext_EapPrfInfo","PSecPkgContext_EapPrfInfo structure pointer [Security]","SecPkgContext_EapPrfInfo","SecPkgContext_EapPrfInfo structure [Security]","schannel/PSecPkgContext_EapPrfInfo","schannel/SecPkgContext_EapPrfInfo","security.secpkgcontext_eapprfinfo"]
old-location: security\secpkgcontext_eapprfinfo.htm
tech.root: security
ms.assetid: 2772b83b-d1d1-4a8e-83d5-1f3dec3d66ac
ms.date: 12/05/2018
ms.keywords: '*PSecPkgContext_EapPrfInfo, EAP-FAST Keying Material, EAP-TTLSv0 Challenge Data, EAP-TTLSv0 Keying Material, PPP EAP TLS Key Data, PSecPkgContext_EapPrfInfo, PSecPkgContext_EapPrfInfo structure pointer [Security], SecPkgContext_EapPrfInfo, SecPkgContext_EapPrfInfo structure [Security], schannel/PSecPkgContext_EapPrfInfo, schannel/SecPkgContext_EapPrfInfo, security.secpkgcontext_eapprfinfo'
req.header: schannel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: SecPkgContext_EapPrfInfo, *PSecPkgContext_EapPrfInfo
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SecPkgContext_EapPrfInfo
 - schannel/_SecPkgContext_EapPrfInfo
 - PSecPkgContext_EapPrfInfo
 - schannel/PSecPkgContext_EapPrfInfo
 - SecPkgContext_EapPrfInfo
 - schannel/SecPkgContext_EapPrfInfo
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
 - SecPkgContext_EapPrfInfo
---

# SecPkgContext_EapPrfInfo structure


## -description

The <b>SecPkgContext_EapPrfInfo</b> structure specifies the pseudorandom function (PRF) and extracts key data used by the Extensible Authentication Protocol (EAP) <a href="/windows/desktop/SecGloss/t-gly">Transport Layer Security protocol</a> (TLS) Authentication Protocol. For information about the EAP TLS Authentication Protocol, see <a href="https://www.ietf.org/rfc/rfc2716.txt">http://www.ietf.org/rfc/rfc2716.txt</a>.

## -struct-fields

### -field dwVersion

Reserved. Must be set to zero.

### -field cbPrfData

The size, in bytes, of the <i>pbPrfData</i> array.



#### pbPrfData

A <b>DWORD</b> value that specifies the pseudorandom function and key data used by the EAP protocol. The following are possible values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_EAP_TLS_Key_Data"></a><a id="ppp_eap_tls_key_data"></a><a id="PPP_EAP_TLS_KEY_DATA"></a><dl>
<dt><b>PPP EAP TLS Key Data</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
PRF(master secret, "client EAP encryption", client_random + server_random)

</td>
</tr>
<tr>
<td width="40%"><a id="EAP-TTLSv0_Keying_Material"></a><a id="eap-ttlsv0_keying_material"></a><a id="EAP-TTLSV0_KEYING_MATERIAL"></a><dl>
<dt><b>EAP-TTLSv0 Keying Material</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
PRF(master_secret, "ttls keying material", server_random + client_random)

</td>
</tr>
<tr>
<td width="40%"><a id="EAP-TTLSv0_Challenge_Data"></a><a id="eap-ttlsv0_challenge_data"></a><a id="EAP-TTLSV0_CHALLENGE_DATA"></a><dl>
<dt><b>EAP-TTLSv0 Challenge Data</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
PRF(master_secret, "ttls challenge", server_random + client_random)

</td>
</tr>
<tr>
<td width="40%"><a id="EAP-FAST_Keying_Material"></a><a id="eap-fast_keying_material"></a><a id="EAP-FAST_KEYING_MATERIAL"></a><dl>
<dt><b>EAP-FAST Keying Material</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
PRF(master_secret, "key expansion", server_random + client_random)

</td>
</tr>
</table>

### -field pbPrfData