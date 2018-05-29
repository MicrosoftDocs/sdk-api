---
UID: NS:ipsectypes.IPSEC_SA_TRANSFORM0_
title: IPSEC_SA_TRANSFORM0_
author: windows-sdk-content
description: Is used to store an IPsec security association (SA) transform in an IPsec quick mode policy.
old-location: fwp\ipsec_sa_transform0_struct.htm
old-project: FWP
ms.assetid: 1cf64805-e79d-4599-addf-0ad24d7d900e
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_SA_TRANSFORM0, IPSEC_SA_TRANSFORM0 structure [Filtering], IPSEC_SA_TRANSFORM0_, fwp.ipsec_sa_transform0_struct, ipsectypes/IPSEC_SA_TRANSFORM0
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: IPSEC_SA_TRANSFORM0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_SA_TRANSFORM0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA_TRANSFORM0_ structure


## -description


The <b>IPSEC_SA_TRANSFORM0</b> structure is used to store an IPsec security association (SA) transform in an IPsec quick mode policy.


## -struct-fields




### -field ipsecTransformType

Type of the SA transform.

See <a href="https://msdn.microsoft.com/068f17f2-8696-4419-9daa-d8f6486e39a3">IPSEC_TRANSFORM_TYPE</a> for more information.


### -field ahTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_AH</b>.

See <a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a> for more information.


### -field espAuthTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH</b>.

See <a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a> for more information.


### -field espCipherTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_CIPHER</b>.

See <a href="https://msdn.microsoft.com/d8a9515a-943b-4f00-bfa9-948a9da9c060">IPSEC_CIPHER_TRANSFORM0</a> for more information.


### -field espAuthAndCipherTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER</b>.

See <a href="https://msdn.microsoft.com/9f8086c3-1862-432a-af0e-6a434833c651">IPSEC_AUTH_AND_CIPHER_TRANSFORM0</a> for more information.


### -field espAuthFwTransform

SA transform data. Available when <b>ipsecTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_FW</b>.

See <a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a> for more information.


<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, or later.</div>
<div> </div>



## -remarks



<b>IPSEC_SA_TRANSFORM0</b> is a specific implementation of IPSEC_SA_TRANSFORM. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/9f8086c3-1862-432a-af0e-6a434833c651">IPSEC_AUTH_AND_CIPHER_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/d8a9515a-943b-4f00-bfa9-948a9da9c060">IPSEC_CIPHER_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/068f17f2-8696-4419-9daa-d8f6486e39a3">IPSEC_TRANSFORM_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

