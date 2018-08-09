---
UID: NS:ipsectypes.IPSEC_SA0_
title: IPSEC_SA0_
author: windows-sdk-content
description: Is used to store information about an IPsec security association (SA).
old-location: fwp\ipsec_sa0_struct.htm
old-project: fwp
ms.assetid: 9d60f5d7-57af-4c33-90ed-b69a9671a9ce
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPSEC_SA0, IPSEC_SA0 structure [Filtering], IPSEC_SA0_, fwp.ipsec_sa0_struct, ipsectypes/IPSEC_SA0
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
tech.root: 
req.typenames: IPSEC_SA0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ipsectypes.h
api_name:
 - IPSEC_SA0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA0_ structure


## -description


The <b>IPSEC_SA0</b> structure is used to store information about an IPsec security association (SA).


## -struct-fields




### -field spi

Security parameter index (SPI) of the IPsec SA. <b>IPSEC_SA_SPI</b> is defined in ipsectypes.h as UINT32.


### -field saTransformType

Transform type of the SA specifying the IPsec security protocol.

See <a href="https://msdn.microsoft.com/068f17f2-8696-4419-9daa-d8f6486e39a3">IPSEC_TRANSFORM_TYPE</a> for more information.


### -field ahInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_AH</b>.

See <a href="https://msdn.microsoft.com/54a03edd-94cb-478a-a647-473872408701">IPSEC_SA_AUTH_INFORMATION0</a> for more information.


### -field espAuthInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH</b>.

See <a href="https://msdn.microsoft.com/54a03edd-94cb-478a-a647-473872408701">IPSEC_SA_AUTH_INFORMATION0</a> for more information.


### -field espCipherInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_CIPHER</b>.

See <a href="https://msdn.microsoft.com/2a5105ad-b77f-46b7-9a79-50514b88e7ce">IPSEC_SA_CIPHER_INFORMATION0</a> for more information.


### -field espAuthAndCipherInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_AND_CIPHER</b>.

See <a href="https://msdn.microsoft.com/0e213ba0-3993-41da-8ddd-5ecde7942a95">IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</a> for more information.


### -field espAuthFwInformation

Security algorithms of the SA transform. Available when <b>saTransformType</b> is <b>IPSEC_TRANSFORM_ESP_AUTH_FW</b>.


<div class="alert"><b>Note</b>  Available only on Windows Server 2008 R2, Windows 7, or later.</div>
<div> </div>



## -remarks



<b>IPSEC_SA0</b> is a specific implementation of IPSEC_SA. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/0e213ba0-3993-41da-8ddd-5ecde7942a95">IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</a>



<a href="https://msdn.microsoft.com/54a03edd-94cb-478a-a647-473872408701">IPSEC_SA_AUTH_INFORMATION0</a>



<a href="https://msdn.microsoft.com/2a5105ad-b77f-46b7-9a79-50514b88e7ce">IPSEC_SA_CIPHER_INFORMATION0</a>



<a href="https://msdn.microsoft.com/068f17f2-8696-4419-9daa-d8f6486e39a3">IPSEC_TRANSFORM_TYPE</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

