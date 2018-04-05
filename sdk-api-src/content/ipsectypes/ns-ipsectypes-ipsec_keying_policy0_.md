---
UID: NS:ipsectypes.IPSEC_KEYING_POLICY0_
title: IPSEC_KEYING_POLICY0_
author: windows-driver-content
description: Defines an unordered set of keying modules that will be tried for IPsec.
old-location: fwp\ipsec_keying_policy0_struct.htm
old-project: FWP
ms.assetid: 6eddafbf-ac57-419f-b2a0-f50a4ab31baf
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IPSEC_KEYING_POLICY0, IPSEC_KEYING_POLICY0 structure [Filtering], IPSEC_KEYING_POLICY0_, fwp.ipsec_keying_policy0_struct, ipsectypes/IPSEC_KEYING_POLICY0
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
req.typenames: IPSEC_KEYING_POLICY0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Ipsectypes.h
api_name:
-	IPSEC_KEYING_POLICY0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPSEC_KEYING_POLICY0_ structure


## -description


The <b>IPSEC_KEYING_POLICY0</b> structure defines an unordered set of keying modules that will be tried for IPsec.<div class="alert"><b>Note</b>  <b>IPSEC_KEYING_POLICY0</b> is the specific implementation of IPSEC_KEYING_POLICY used in Windows Vista and Windows 7. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/4b574e1c-ce0f-4c72-a14b-5ca0ed8aa005">IPSEC_KEYING_POLICY1</a> is available.</div>
<div> </div>



## -struct-fields




### -field numKeyMods

Number of keying modules in the array.


### -field keyModKeys

Array of distinct keying modules.


## -remarks



<b>IPSEC_KEYING_POLICY0</b> is a specific implementation of IPSEC_KEYING_POLICY. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

