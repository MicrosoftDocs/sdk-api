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

# _PPP_CCP_INFO structure


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




<a href="https://msdn.microsoft.com/b6158047-6337-483f-9a90-74d578831772">PPP_LCP_INFO</a>
 

 

