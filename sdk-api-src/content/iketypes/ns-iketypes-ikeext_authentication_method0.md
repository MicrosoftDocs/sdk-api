---
UID: NS:iketypes.IKEEXT_AUTHENTICATION_METHOD0_
title: IKEEXT_AUTHENTICATION_METHOD0 (iketypes.h)
author: windows-sdk-content
description: Specifies various parameters for IKE/AuthIP authentication.
old-location: fwp\ikeext_authentication_method0.htm
tech.root: fwp
ms.assetid: ce11d9ac-2636-432b-9bc7-3509f52478d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IKEEXT_AUTHENTICATION_METHOD0, IKEEXT_AUTHENTICATION_METHOD0 structure [Filtering], fwp.ikeext_authentication_method0, iketypes/IKEEXT_AUTHENTICATION_METHOD0
ms.topic: struct
f1_keywords: 
 - "iketypes/IKEEXT_AUTHENTICATION_METHOD0"
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
targetos: Windows
req.typenames: IKEEXT_AUTHENTICATION_METHOD0
req.redist: 
ms.custom: 19H1
---

# IKEEXT_AUTHENTICATION_METHOD0 structure


## -description


The <b>IKEEXT_AUTHENTICATION_METHOD0</b> structure specifies various parameters for IKE/AuthIP authentication.<div class="alert"><b>Note</b>  <b>IKEEXT_AUTHENTICATION_METHOD0</b> is the specific implementation of IKEEXT_AUTHENTICATION_METHOD used in Windows Vista. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-version-independent-names-and-targeting-specific-versions-of-windows">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method1_">IKEEXT_AUTHENTICATION_METHOD1</a> is available.For Windows 8, <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_authentication_method2_">IKEEXT_AUTHENTICATION_METHOD2</a> is available. </div>
<div> </div>



## -struct-fields




### -field authenticationMethodType

Type of authentication method specified by <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ne-iketypes-ikeext_authentication_method_type">IKEEXT_AUTHENTICATION_METHOD_TYPE</a>.


### -field presharedKeyAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_PRESHARED_KEY</b>.

See <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ns-iketypes-ikeext_preshared_key_authentication0">IKEEXT_PRESHARED_KEY_AUTHENTICATION0</a> for more information.


### -field certificateAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_CERTIFICATE</b>, <b>IKEEXT_CERTIFICATE_ECDSA_P256</b>, or <b>IKEEXT_CERTIFICATE_ECDSA_P384</b>.

See <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication0">IKEEXT_CERTIFICATE_AUTHENTICATION0</a> for more information.


### -field kerberosAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_KERBEROS</b>.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_kerberos_authentication0__">IKEEXT_KERBEROS_AUTHENTICATION0</a> for more information.


### -field ntlmV2Authentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_NTLM_V2</b>.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_ntlm_v2_authentication0__">IKEEXT_NTLM_V2_AUTHENTICATION0</a> for more information.


### -field sslAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_SSL</b>, <b>IKEEXT_SSL_ECDSA_P256</b>, or <b>IKEEXT_SSL_ECDSA_P384</b>.

See <a href="https://docs.microsoft.com/windows/win32/api/iketypes/ns-iketypes-ikeext_certificate_authentication0">IKEEXT_CERTIFICATE_AUTHENTICATION0</a> for more information.


### -field cgaAuthentication

Available when <b>authenticationMethodType</b> is <b>IKEEXT_IPV6_CGA</b>. Available only for IKE.

See <a href="https://docs.microsoft.com/windows/desktop/api/iketypes/ns-iketypes-ikeext_ipv6_cga_authentication0_">IKEEXT_IPV6_CGA_AUTHENTICATION0</a> for more information.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-structs">Windows Filtering Platform  API Structures</a>
 

 

