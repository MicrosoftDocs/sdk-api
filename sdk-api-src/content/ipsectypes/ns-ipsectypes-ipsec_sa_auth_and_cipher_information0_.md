---
UID: NS:ipsectypes.IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_
title: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_
author: windows-sdk-content
description: Stores information about the authentication and encryption algorithms of an IPsec security association (SA).
old-location: fwp\ipsec_sa_auth_and_cipher_information0_struct.htm
old-project: FWP
ms.assetid: 0e213ba0-3993-41da-8ddd-5ecde7942a95
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0, IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0 structure [Filtering], IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_, fwp.ipsec_sa_auth_and_cipher_information0_struct, ipsectypes/IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
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
req.typenames: IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0_ structure


## -description


The <b>IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</b> structure stores information about the authentication and encryption algorithms of an IPsec security association (SA).


## -struct-fields




### -field saCipherInformation

Encryption algorithm information as specified by <a href="https://msdn.microsoft.com/2a5105ad-b77f-46b7-9a79-50514b88e7ce">IPSEC_SA_CIPHER_INFORMATION0</a>.


### -field saAuthInformation

Authentication algorithm information as specified by <a href="https://msdn.microsoft.com/54a03edd-94cb-478a-a647-473872408701">IPSEC_SA_AUTH_INFORMATION0</a>.


## -remarks



<b>IPSEC_SA_AUTH_AND_CIPHER_INFORMATION0</b> is a specific implementation of IPSEC_SA_AUTH_AND_CIPHER_INFORMATION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/54a03edd-94cb-478a-a647-473872408701">IPSEC_SA_AUTH_INFORMATION0</a>



<a href="https://msdn.microsoft.com/2a5105ad-b77f-46b7-9a79-50514b88e7ce">IPSEC_SA_CIPHER_INFORMATION0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

