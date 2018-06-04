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

# IKEEXT_AUTHENTICATION_METHOD2_ structure


## -description


The <b>IKEEXT_AUTHENTICATION_METHOD2</b> structure specifies various parameters for IKE/Authip authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_AUTHENTICATION_METHOD2</b> is the specific implementation of IKEEXT_AUTHENTICATION_METHOD used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/55894ac3-2cb7-4828-8346-9ca66ce3253a">IKEEXT_AUTHENTICATION_METHOD1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/ce11d9ac-2636-432b-9bc7-3509f52478d9">IKEEXT_AUTHENTICATION_METHOD0</a>  is available.</div><div> </div>

## -struct-fields




### -field authenticationMethodType

Type: <b><a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a></b>

Type of authentication method.


### -field presharedKeyAuthentication

Type: <b><a href="https://msdn.microsoft.com/b2009797-f5fd-4d14-8a59-832f9a0acff1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a></b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.


### -field certificateAuthentication

Type: <b><a href="https://msdn.microsoft.com/39332187-6562-4f58-9284-e2aaccf1489b">IKEEXT_CERTIFICATE_AUTHENTICATION2</a></b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_CERTIFICATE</b>, <b>IKEEXT_CERTIFICATE_ECDSA_P256</b>, or <b>IKEEXT_CERTIFICATE_ECDSA_P384</b>.


### -field kerberosAuthentication

Type: <b><a href="https://msdn.microsoft.com/c9ea72e1-3d98-49f1-9061-d19e16f50660">IKEEXT_KERBEROS_AUTHENTICATION1</a></b>

 Available when <b>authenticationMethodType</b> is <b>IKEEXT_KERBEROS</b>.


### -field reservedAuthentication

Type: <b><a href="https://msdn.microsoft.com/afae9b31-363a-47d9-9fc9-18efd8332fce">IKEEXT_RESERVED_AUTHENTICATION0</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_RESERVED</b>.


### -field ntlmV2Authentication

Type: <b><a href="https://msdn.microsoft.com/8ac34054-5066-49f2-80b6-e674f6175c8e">IKEEXT_NTLM_V2_AUTHENTICATION0</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_NTLM_V2</b>.


### -field sslAuthentication

Type: <b><a href="https://msdn.microsoft.com/39332187-6562-4f58-9284-e2aaccf1489b">IKEEXT_CERTIFICATE_AUTHENTICATION2</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_SSL</b>, <b>IKEEXT_SSL_ECDSA_P256</b>, or <b>IKEEXT_SSL_ECDSA_P384</b>.


### -field cgaAuthentication

Type: <b><a href="https://msdn.microsoft.com/6b472140-f3e3-45b9-81f3-9c428b687fe4">IKEEXT_IPV6_CGA_AUTHENTICATION0</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_IPV6_CGA</b>.


### -field eapAuthentication

Type: <b><a href="https://msdn.microsoft.com/86029526-ea87-4962-b5f5-f535c7034c60">IKEEXT_EAP_AUTHENTICATION0</a></b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_EAP</b>.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

