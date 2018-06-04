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

# _IKEV2_TUNNEL_CONFIG_PARAMS2 structure


## -description


Gets or sets tunnel parameters for Internet Key Exchange version 2 (IKEv2) devices.

Do not use the <b>IKEV2_TUNNEL_CONFIG_PARAMS2</b> structure directly in your code; using <a href="https://msdn.microsoft.com/6CF919BD-E1E9-423F-8186-C992A5E6AB89">IKEV2_TUNNEL_CONFIG_PARAMS</a> instead ensures that the proper version, based on the operating system the code in compiled under, is used.


## -struct-fields




### -field dwIdleTimeout

A value that specifies the time, in seconds, after which the connection will be disconnected if there is no traffic.


### -field dwNetworkBlackoutTime

A value that specifies the retransmission timeout for IKEv2 request packets. IKEv2 expects a response for every request packet sent, this value specifies the time after which the connection is deleted in case a response is not received.


### -field dwSaLifeTime

A value that specifies the lifetime, in seconds, of a security association (SA), after which the SA is no longer valid.


### -field dwSaDataSizeForRenegotiation

A value that specifies the number of kilobytes that are allowed to be transferred using a SA before it must be renegotiated.


### -field dwConfigOptions

Not implemented. Must be set to 0.


### -field dwTotalCertificates

A value that specifies the number of certificates in <b>certificateNames</b>.


### -field certificateNames

An array of CERT_NAME_BLOB structures that contain X.509 public key infrastructure certificates.


### -field machineCertificateName

The encryption type to be used for IKEv2.


### -field dwEncryptionType

A value that  that specifies the encryption type to be negotiated during  the SA negotiation for the IKE2 tunnel based VPN connections. The <i>dwEncryptionType</i> parameter must have one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
RRAS will not negotiate encryption.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
RRAS requests encryption during negotiation. Negotiation will succeed even if remote RRAS does not support encryption.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
RRAS requires encryption to be negotiated.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
RRAS requires maximum strength encryption to be negotiated.

</td>
</tr>
</table>
 


### -field customPolicy

A value that specifies the custom IKEv2 configurations to be used during  the SA negotiation. If <b>customPolicy</b> is set to <b>NULL</b>, no custom IKEv2 configuration is available.

