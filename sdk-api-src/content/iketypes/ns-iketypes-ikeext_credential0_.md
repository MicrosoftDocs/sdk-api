---
UID: NS:iketypes.IKEEXT_CREDENTIAL0_
title: IKEEXT_CREDENTIAL0_
author: windows-sdk-content
description: Is used to store credential information used for the authentication.
old-location: fwp\ikeext_credential0.htm
tech.root: fwp
ms.assetid: cb5aa4b6-71e7-43d4-a69c-4f209cd9755b
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IKEEXT_CREDENTIAL0, IKEEXT_CREDENTIAL0 structure [Filtering], IKEEXT_CREDENTIAL0_, fwp.ikeext_credential0, iketypes/IKEEXT_CREDENTIALS0
ms.prod: windows
ms.technology: windows-sdk
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
 - IKEEXT_CREDENTIAL0
product: Windows
targetos: Windows
req.typenames: IKEEXT_CREDENTIAL0
req.redist: 
---

# IKEEXT_CREDENTIAL0_ structure


## -description


The <b>IKEEXT_CREDENTIAL0</b> structure is  used to store credential information used for the authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIAL0</b> is the specific implementation of IKEEXT_CREDENTIAL used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/b27689ef-5e2a-4163-a4d7-40f8939d4c66">IKEEXT_CREDENTIAL2</a> is available.</div><div> </div>

## -struct-fields




### -field authenticationMethodType

Type of authentication method.

See <a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a> for more information.


### -field impersonationType

Type of impersonation.

See <a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a> for more information.


### -field presharedKey

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

See <a href="https://msdn.microsoft.com/44cd2a76-cd8a-4c52-af41-927b13862c1e">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a> for more information.


### -field certificate

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_CERTIFICATE</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P256</b>
<b>IKEEXT_CERTIFICATE_ECDSA_P384</b>
<b>IKEEXT_SSL</b>
<b>IKEEXT_SSL_ECDSA_P256</b>
<b>IKEEXT_SSL_ECDSA_P384</b>
<b>IKEEXT_IPV6_CGA</b>
See <a href="https://msdn.microsoft.com/926a7e74-a225-4234-8be0-c8731840756a">IKEEXT_CERTIFICATE_CREDENTIAL0</a> for more information.


### -field name

Available when <b>authenticationMethodType</b> is one of the following values.

<b>IKEEXT_KERBEROS</b>
<b>IKEEXT_NTML_V2</b>
See <a href="https://msdn.microsoft.com/602f94bf-066d-418e-a469-a21b881a443d">IKEEXT_NAME_CREDENTIAL0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/840c7429-5a1a-4e3f-823c-c46a412cbe71">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="https://msdn.microsoft.com/582ec1ea-9390-4f86-9a3c-25d4e805a218">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



<a href="https://msdn.microsoft.com/926a7e74-a225-4234-8be0-c8731840756a">IKEEXT_CERTIFICATE_CREDENTIAL0</a>



<a href="https://msdn.microsoft.com/602f94bf-066d-418e-a469-a21b881a443d">IKEEXT_NAME_CREDENTIAL0</a>



<a href="https://msdn.microsoft.com/44cd2a76-cd8a-4c52-af41-927b13862c1e">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

