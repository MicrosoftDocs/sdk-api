---
UID: NS:wincrypt._CERT_BIOMETRIC_EXT_INFO
title: "_CERT_BIOMETRIC_EXT_INFO"
author: windows-sdk-content
description: Contains a set of biometric information.
old-location: security\cert_biometric_ext_info.htm
tech.root: seccrypto
ms.assetid: b2a877e1-2be2-428c-bc47-ec5ce6cef7e6
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: "*PCERT_BIOMETRIC_EXT_INFO, CERT_BIOMETRIC_EXT_INFO, CERT_BIOMETRIC_EXT_INFO structure [Security], PCERT_BIOMETRIC_EXT_INFO, PCERT_BIOMETRIC_EXT_INFO structure pointer [Security], _CERT_BIOMETRIC_EXT_INFO, security.cert_biometric_ext_info, wincrypt/CERT_BIOMETRIC_EXT_INFO, wincrypt/PCERT_BIOMETRIC_EXT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_BIOMETRIC_EXT_INFO
product: Windows
targetos: Windows
req.typenames: CERT_BIOMETRIC_EXT_INFO, *PCERT_BIOMETRIC_EXT_INFO
req.redist: 
---

# _CERT_BIOMETRIC_EXT_INFO structure


## -description


The <b>CERT_BIOMETRIC_EXT_INFO</b> structure contains a set of biometric information.


## -struct-fields




### -field cBiometricData

The number of elements in the <b>rgBiometricData</b> array.


### -field rgBiometricData

An array of <a href="https://msdn.microsoft.com/544297e2-b6a6-4a33-94b6-47066262506a">CERT_BIOMETRIC_DATA</a> structures that contain the biometric data. The <b>cBiometricData</b> member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>
 

 

