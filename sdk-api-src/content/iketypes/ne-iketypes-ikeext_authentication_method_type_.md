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

# IKEEXT_AUTHENTICATION_METHOD_TYPE_ enumeration


## -description


The <b>IKEEXT_AUTHENTICATION_METHOD_TYPE</b> enumerated type specifies the type of authentication method used by Internet Key Exchange (IKE), Authenticated Internet Protocol (AuthIP), or IKEv2..


## -enum-fields




### -field IKEEXT_PRESHARED_KEY

Specifies pre-shared key authentication method. Available only for IKE.


### -field IKEEXT_CERTIFICATE

Specifies certificate authentication method. Available only for IKE and IKEv2.


### -field IKEEXT_KERBEROS

Specifies Kerberos authentication method.


### -field IKEEXT_ANONYMOUS

Specifies anonymous authentication method. Available only for AuthIP.


### -field IKEEXT_SSL

Specifies Secure Sockets Layer (SSL) authentication method. Available only for AuthIP.


### -field IKEEXT_NTLM_V2

Specifies Microsoft Windows NT LAN Manager (NTLM) V2 authentication method. Available only for AuthIP.


### -field IKEEXT_IPV6_CGA

Specifies IPv6 Cryptographically Generated Addresses (CGA) authentication method. Available only for IKE.


### -field IKEEXT_CERTIFICATE_ECDSA_P256

Specifies Elliptic Curve Digital Signature Algorithm (ECDSA) 256 certificate authentication method. Available only for IKE and IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_CERTIFICATE_ECDSA_P384

Specifies ECDSA-384 certificate authentication method. Available only for IKE and IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_SSL_ECDSA_P256

Specifies ECDSA-256 SSL authentication method. Available only for AuthIP.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_SSL_ECDSA_P384

Specifies ECDSA-384 SSL authentication method. Available only for AuthIP.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008, Windows Vista with SP1, and later.</div>
<div> </div>

### -field IKEEXT_EAP

Specifies Extensible Authentication Protocol (EAP) authentication method. Available only for IKEv2.

<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, and later.</div>
<div> </div>

### -field IKEEXT_RESERVED

Reserved. Do not use.

<div class="alert"><b>Note</b>  Available only on Windows Server 2012, Windows 8, and later.</div>
<div> </div>

### -field IKEEXT_AUTHENTICATION_METHOD_TYPE_MAX

Maximum value for testing purposes.


## -see-also




<a href="https://msdn.microsoft.com/39029412-18ce-426a-a79d-cf25ff0dfe0d">Windows Filtering Platform API Enumerated Types</a>
 

 

