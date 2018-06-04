---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IKEEXT_CREDENTIALS0_ structure


## -description


The <b>IKEEXT_CREDENTIALS0</b> structure is used to store multiple credential pairs.  
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIALS0</b> is the specific implementation of IKEEXT_CREDENTIALS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/dbd895bd-a720-4c8e-a2e7-f5614d69922c">IKEEXT_CREDENTIALS1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/4099b6e7-0b3b-40ea-821c-3ff28a6f788f">IKEEXT_CREDENTIALS2</a> is available.</div><div> </div>

## -struct-fields




### -field numCredentials

Number of <a href="https://msdn.microsoft.com/35dcc31f-8acd-4b7d-901d-3b2e9cde1690">IKEEXT_CREDENTIAL_PAIR0</a> structures in the array.


### -field credentials

[size_is(numCredentials)]

Pointer to an array of <a href="https://msdn.microsoft.com/35dcc31f-8acd-4b7d-901d-3b2e9cde1690">IKEEXT_CREDENTIAL_PAIR0</a> structures.


## -remarks



IKE has only 1 pair.

AuthIP
has 1 pair, or 2 pairs if EM was enabled.

MM authentication is always index 0.

EM authentication, if it occurs,
is index 1.




## -see-also




<a href="https://msdn.microsoft.com/35dcc31f-8acd-4b7d-901d-3b2e9cde1690">IKEEXT_CREDENTIAL_PAIR0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

