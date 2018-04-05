---
UID: NS:iketypes.IKEEXT_CREDENTIAL_PAIR1_
title: IKEEXT_CREDENTIAL_PAIR1_
author: windows-driver-content
description: Is used to store credential information used for the authentication.
old-location: fwp\ikeext_credential_pair1.htm
old-project: FWP
ms.assetid: fe18503d-fd1c-45b6-86c7-9b452036f8c8
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IKEEXT_CREDENTIAL_PAIR1, IKEEXT_CREDENTIAL_PAIR1 structure [Filtering], IKEEXT_CREDENTIAL_PAIR1_, fwp.ikeext_credential_pair1, iketypes/IKEEXT_CREDENTIAL_PAIR1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_CREDENTIAL_PAIR1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_CREDENTIAL_PAIR1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_CREDENTIAL_PAIR1_ structure


## -description


The <b>IKEEXT_CREDENTIAL_PAIR1</b> structure is  used to store credential information used for the authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIAL_PAIR1</b> is the specific implementation of IKEEXT_CREDENTIAL_PAIR used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 8, <a href="https://msdn.microsoft.com/013b7b6c-aee6-40f3-b8c4-ef98784165ca">IKEEXT_CREDENTIAL_PAIR2</a> is available. For Windows Vista, <a href="https://msdn.microsoft.com/35dcc31f-8acd-4b7d-901d-3b2e9cde1690">IKEEXT_CREDENTIAL_PAIR0</a> is available.</div><div> </div>

## -struct-fields




### -field localCredentials

Local credentials used for authentication.

See <a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a> for more information.


### -field peerCredentials

Peer credentials used for authentication.

See <a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/81b4c66a-67dd-4d5a-bd71-2fdbe6fd5df5">IKEEXT_CREDENTIAL1</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

