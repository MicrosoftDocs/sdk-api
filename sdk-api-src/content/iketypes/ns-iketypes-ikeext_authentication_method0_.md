---
UID: NS:iketypes.IKEEXT_AUTHENTICATION_METHOD0_
title: IKEEXT_AUTHENTICATION_METHOD0_
author: windows-sdk-content
description: Specifies various parameters for IKE/AuthIP authentication.
old-location: fwp\ikeext_authentication_method0.htm
tech.root: fwp
ms.assetid: ce11d9ac-2636-432b-9bc7-3509f52478d9
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IKEEXT_AUTHENTICATION_METHOD0, IKEEXT_AUTHENTICATION_METHOD0 structure [Filtering], IKEEXT_AUTHENTICATION_METHOD0_, fwp.ikeext_authentication_method0, iketypes/IKEEXT_AUTHENTICATION_METHOD0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_AUTHENTICATION_METHOD0
product: Windows
targetos: Windows
req.typenames: IKEEXT_AUTHENTICATION_METHOD0
req.redist: 
---

# IKEEXT_AUTHENTICATION_METHOD0_ structure


## -description


The <b>IKEEXT_AUTHENTICATION_METHOD0</b> structure specifies various parameters for IKE/AuthIP authentication.<div class="alert"><b>Note</b>  <b>IKEEXT_AUTHENTICATION_METHOD0</b> is the specific implementation of IKEEXT_AUTHENTICATION_METHOD used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/55894ac3-2cb7-4828-8346-9ca66ce3253a">IKEEXT_AUTHENTICATION_METHOD1</a> is available.For Windows 8, <a href="https://msdn.microsoft.com/f0bd649e-746d-4802-87fe-d8baec2b252f">IKEEXT_AUTHENTICATION_METHOD2</a> is available. </div>
<div> </div>



## -struct-fields




### -field authenticationMethodType

Type of authentication method specified by <a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>.


### -field presharedKeyAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

See <a href="https://msdn.microsoft.com/44cd2a76-cd8a-4c52-af41-927b13862c1e">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a> for more information.


### -field certificateAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_CERTIFICATE</b>, <b>IKEEXT_CERTIFICATE_ECDSA_P256</b>, or <b>IKEEXT_CERTIFICATE_ECDSA_P384</b>.

See <a href="https://msdn.microsoft.com/e9f9625d-b68b-4b7d-a587-39dac04dd991">IKEEXT_CERTIFICATE_AUTHENTICATION0</a> for more information.


### -field kerberosAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_KERBEROS</b>.

See <a href="https://msdn.microsoft.com/2dd626c2-4b70-450a-ad6a-a978f1d93bbf">IKEEXT_KERBEROS_AUTHENTICATION0</a> for more information.


### -field ntlmV2Authentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_NTLM_V2</b>.

See <a href="https://msdn.microsoft.com/8ac34054-5066-49f2-80b6-e674f6175c8e">IKEEXT_NTLM_V2_AUTHENTICATION0</a> for more information.


### -field sslAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_SSL</b>, <b>IKEEXT_SSL_ECDSA_P256</b>, or <b>IKEEXT_SSL_ECDSA_P384</b>.

See <a href="https://msdn.microsoft.com/e9f9625d-b68b-4b7d-a587-39dac04dd991">IKEEXT_CERTIFICATE_AUTHENTICATION0</a> for more information.


### -field cgaAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_IPV6_CGA</b>. Available only for IKE.

See <a href="https://msdn.microsoft.com/6b472140-f3e3-45b9-81f3-9c428b687fe4">IKEEXT_IPV6_CGA_AUTHENTICATION0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

