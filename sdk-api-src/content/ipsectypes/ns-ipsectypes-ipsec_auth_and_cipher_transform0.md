---
UID: NS:ipsectypes.IPSEC_AUTH_AND_CIPHER_TRANSFORM0_
title: IPSEC_AUTH_AND_CIPHER_TRANSFORM0
author: windows-sdk-content
description: Is used to store hash and encryption specific information together for an SA transform in an IPsec quick mode policy.
old-location: fwp\ipsec_auth_and_cipher_transform0_struct.htm
tech.root: fwp
ms.assetid: 9f8086c3-1862-432a-af0e-6a434833c651
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPSEC_AUTH_AND_CIPHER_TRANSFORM0, IPSEC_AUTH_AND_CIPHER_TRANSFORM0 structure [Filtering], fwp.ipsec_auth_and_cipher_transform0_struct, ipsectypes/IPSEC_AUTH_AND_CIPHER_TRANSFORM0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: ipsectypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ipsectypes.idl
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
 - Ipsectypes.h
api_name:
 - IPSEC_AUTH_AND_CIPHER_TRANSFORM0
product: Windows
targetos: Windows
req.typenames: IPSEC_AUTH_AND_CIPHER_TRANSFORM0
req.redist: 
---

# IPSEC_AUTH_AND_CIPHER_TRANSFORM0 structure


## -description


The <b>IPSEC_AUTH_AND_CIPHER_TRANSFORM0</b> structure is used to store hash and encryption specific information together for an SA
transform in an IPsec quick mode policy.


## -struct-fields




### -field authTransform

Hash specific information as specified by <a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a>.


### -field cipherTransform

Encryption specific information as specified by <a href="https://msdn.microsoft.com/d8a9515a-943b-4f00-bfa9-948a9da9c060">IPSEC_CIPHER_TRANSFORM0</a>.


## -remarks



<b>IPSEC_AUTH_AND_CIPHER_TRANSFORM0</b> is a specific implementation of IPSEC_AUTH_AND_CIPHER_TRANSFORM. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/d8a9515a-943b-4f00-bfa9-948a9da9c060">IPSEC_CIPHER_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

