---
UID: NS:mprapi._PPP_CCP_INFO
title: PPP_CCP_INFO (mprapi.h)
description: The PPP_CCP_INFO structure contains information that describes the results of a Compression Control Protocol (CCP) negotiation.
helpviewer_keywords: ["PPP_CCP_COMPRESSION","PPP_CCP_ENCRYPTION128BIT","PPP_CCP_ENCRYPTION40BIT","PPP_CCP_ENCRYPTION40BITOLD","PPP_CCP_ENCRYPTION56BIT","PPP_CCP_HISTORYLESS","PPP_CCP_INFO","PPP_CCP_INFO structure [RAS]","RASCCPCA_MPPC","RASCCPCA_STAC","_mpr_ppp_ccp_info","mprapi/PPP_CCP_INFO","rras.ppp_ccp_info"]
old-location: rras\ppp_ccp_info.htm
tech.root: RRAS
ms.assetid: d50493c4-8a18-4cab-8973-a752f3f7f6c2
ms.date: 12/05/2018
ms.keywords: PPP_CCP_COMPRESSION, PPP_CCP_ENCRYPTION128BIT, PPP_CCP_ENCRYPTION40BIT, PPP_CCP_ENCRYPTION40BITOLD, PPP_CCP_ENCRYPTION56BIT, PPP_CCP_HISTORYLESS, PPP_CCP_INFO, PPP_CCP_INFO structure [RAS], RASCCPCA_MPPC, RASCCPCA_STAC, _mpr_ppp_ccp_info, mprapi/PPP_CCP_INFO, rras.ppp_ccp_info
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
req.typenames: PPP_CCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_CCP_INFO
 - mprapi/_PPP_CCP_INFO
 - PPP_CCP_INFO
 - mprapi/PPP_CCP_INFO
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
 - PPP_CCP_INFO
---

# PPP_CCP_INFO structure


## -description

The 
<b>PPP_CCP_INFO</b> structure contains information that describes the results of a Compression Control Protocol (CCP) negotiation.

## -struct-fields

### -field dwError

Specifies an error if the negotiation is unsuccessful.

### -field dwCompressionAlgorithm

Specifies the compression algorithm used by the local computer. The following table shows the possible values for this member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_MPPC"></a><a id="rasccpca_mppc"></a><dl>
<dt><b>RASCCPCA_MPPC</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Compression (MPPC) Protocol

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_STAC"></a><a id="rasccpca_stac"></a><dl>
<dt><b>RASCCPCA_STAC</b></dt>
</dl>
</td>
<td width="60%">
STAC option 4

</td>
</tr>
</table>

### -field dwOptions

Specifies the compression options on the local computer. The following options are supported. 



<table>
<tr>
<th>Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_COMPRESSION"></a><a id="ppp_ccp_compression"></a><dl>
<dt><b>PPP_CCP_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_HISTORYLESS"></a><a id="ppp_ccp_historyless"></a><dl>
<dt><b>PPP_CCP_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BITOLD"></a><a id="ppp_ccp_encryption40bitold"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BIT"></a><a id="ppp_ccp_encryption40bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION56BIT"></a><a id="ppp_ccp_encryption56bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION128BIT"></a><a id="ppp_ccp_encryption128bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 128-bit keys.

</td>
</tr>
</table>

### -field dwRemoteCompressionAlgorithm

Specifies the compression algorithm used by the remote computer. The following table shows the possible values for this member. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_MPPC"></a><a id="rasccpca_mppc"></a><dl>
<dt><b>RASCCPCA_MPPC</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Compression (MPPC) Protocol

</td>
</tr>
<tr>
<td width="40%"><a id="RASCCPCA_STAC"></a><a id="rasccpca_stac"></a><dl>
<dt><b>RASCCPCA_STAC</b></dt>
</dl>
</td>
<td width="60%">
STAC option 4

</td>
</tr>
</table>

### -field dwRemoteOptions

Specifies the compression options on the remote computer. The following options are supported. 



<table>
<tr>
<th>Option</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_COMPRESSION"></a><a id="ppp_ccp_compression"></a><dl>
<dt><b>PPP_CCP_COMPRESSION</b></dt>
</dl>
</td>
<td width="60%">
Compression without encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_HISTORYLESS"></a><a id="ppp_ccp_historyless"></a><dl>
<dt><b>PPP_CCP_HISTORYLESS</b></dt>
</dl>
</td>
<td width="60%">
Microsoft Point-to-Point Encryption (MPPE) in stateless mode. The session key is changed after every packet. This mode improves performance on high latency networks, or networks that experience significant packet loss.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BITOLD"></a><a id="ppp_ccp_encryption40bitold"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BITOLD</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION40BIT"></a><a id="ppp_ccp_encryption40bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION40BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 40-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION56BIT"></a><a id="ppp_ccp_encryption56bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION56BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 56-bit keys.

</td>
</tr>
<tr>
<td width="40%"><a id="PPP_CCP_ENCRYPTION128BIT"></a><a id="ppp_ccp_encryption128bit"></a><dl>
<dt><b>PPP_CCP_ENCRYPTION128BIT</b></dt>
</dl>
</td>
<td width="60%">
MPPE using 128-bit keys.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_lcp_info">PPP_LCP_INFO</a>