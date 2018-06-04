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

# IKEEXT_CREDENTIAL2_ structure


## -description


The <b>IKEEXT_CREDENTIAL2</b> structure is  used to store credential information used for the authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIAL2</b> is the specific implementation of IKEEXT_CREDENTIAL used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/cb5aa4b6-71e7-43d4-a69c-4f209cd9755b">IKEEXT_CREDENTIAL0</a>  is available.</div><div> </div>

## -struct-fields




### -field authenticationMethodType

Type: <b><a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a></b>

Type of authentication method.


### -field impersonationType

Type: <b><a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation.


### -field presharedKey

Type: <b><a href="https://msdn.microsoft.com/b2009797-f5fd-4d14-8a59-832f9a0acff1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>*</b>

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.


### -field certificate

Type: <b><a href="https://msdn.microsoft.com/78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0">IKEEXT_CERTIFICATE_CREDENTIAL1</a>*</b>

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_CERTIFICATE</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P256</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P384</b>
<b>IKEEXT_SSL</b>
<b>IKEEXT_SSL_ECDSA_P256</b>
<b>IKEEXT_SSL_ECDSA_P384</b>
<b>IKEEXT_IPV6_CGA</b>

### -field name

Type: <b><a href="https://msdn.microsoft.com/602f94bf-066d-418e-a469-a21b881a443d">IKEEXT_NAME_CREDENTIAL0</a>*</b>

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_KERBEROS</b>
<b>IKEEXT_NTML_V2</b>
<b>IKEEXT_RESERVED</b>

## -see-also




<a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



<a href="https://msdn.microsoft.com/78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0">IKEEXT_CERTIFICATE_CREDENTIAL1</a>



<a href="https://msdn.microsoft.com/602f94bf-066d-418e-a469-a21b881a443d">IKEEXT_NAME_CREDENTIAL0</a>



<a href="https://msdn.microsoft.com/b2009797-f5fd-4d14-8a59-832f9a0acff1">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

