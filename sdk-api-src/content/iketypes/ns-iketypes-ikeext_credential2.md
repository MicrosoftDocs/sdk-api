---
UID: NS:iketypes.IKEEXT_CREDENTIAL2_
title: IKEEXT_CREDENTIAL2 (iketypes.h)
author: windows-sdk-content
description: Is used to store credential information used for the authentication.
old-location: fwp\ikeext_credential2.htm
tech.root: fwp
ms.assetid: b27689ef-5e2a-4163-a4d7-40f8939d4c66
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IKEEXT_CREDENTIAL2, IKEEXT_CREDENTIAL2 structure [Filtering], fwp.ikeext_credential2, iketypes/IKEEXT_CREDENTIAL2
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - iketypes.h
api_name:
 - IKEEXT_CREDENTIAL2
product: Windows
targetos: Windows
req.typenames: IKEEXT_CREDENTIAL2
req.redist: 
---

# IKEEXT_CREDENTIAL2 structure


## -description


The <b>IKEEXT_CREDENTIAL2</b> structure is  used to store credential information used for the authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIAL2</b> is the specific implementation of IKEEXT_CREDENTIAL used in Windows 8. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/cb5aa4b6-71e7-43d4-a69c-4f209cd9755b">IKEEXT_CREDENTIAL0</a>  is available.</div><div> </div>

## -struct-fields




### -field authenticationMethodType

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa364977(v=VS.85).aspx">IKEEXT_AUTHENTICATION_METHOD_TYPE</a></b>

Type of authentication method.


### -field impersonationType

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa364974(v=VS.85).aspx">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a></b>

Type of impersonation.


### -field presharedKey

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd744976(v=VS.85).aspx">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>*</b>

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




<a href="https://msdn.microsoft.com/en-us/library/Aa364974(v=VS.85).aspx">IKEEXT_AUTHENTICATION_IMPERSONATION_TYPE</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa364977(v=VS.85).aspx">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>



<a href="https://msdn.microsoft.com/78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0">IKEEXT_CERTIFICATE_CREDENTIAL1</a>



<a href="https://msdn.microsoft.com/602f94bf-066d-418e-a469-a21b881a443d">IKEEXT_NAME_CREDENTIAL0</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd744976(v=VS.85).aspx">IKEEXT_PRESHARED_KEY_AUTHENTICATION1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

