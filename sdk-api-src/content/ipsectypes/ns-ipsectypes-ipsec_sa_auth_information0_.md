---
UID: NS:ipsectypes.IPSEC_SA_AUTH_INFORMATION0_
title: IPSEC_SA_AUTH_INFORMATION0_
author: windows-sdk-content
description: Stores information about the authentication algorithm of an IPsec security association (SA).
old-location: fwp\ipsec_sa_auth_information0_struct.htm
tech.root: fwp
ms.assetid: 54a03edd-94cb-478a-a647-473872408701
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPSEC_SA_AUTH_INFORMATION0, IPSEC_SA_AUTH_INFORMATION0 structure [Filtering], IPSEC_SA_AUTH_INFORMATION0_, fwp.ipsec_sa_auth_information0_struct, ipsectypes/IPSEC_SA_AUTH_INFORMATION0
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
 - IPSEC_SA_AUTH_INFORMATION0
product: Windows
targetos: Windows
req.typenames: IPSEC_SA_AUTH_INFORMATION0
req.redist: 
---

# IPSEC_SA_AUTH_INFORMATION0_ structure


## -description


The <b>IPSEC_SA_AUTH_INFORMATION0</b> structure stores information about the authentication algorithm of an IPsec security association (SA).


## -struct-fields




### -field authTransform

Authentication algorithm details as specified by <a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a>.


### -field authKey

Key used for the authentication algorithm stored in a <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> structure.


## -remarks



<b>IPSEC_SA_AUTH_INFORMATION0</b> is a specific implementation of IPSEC_SA_AUTH_INFORMATION. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/26464393-7dc4-4a94-af46-25148c61bdb5">IPSEC_AUTH_TRANSFORM0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

