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

# IKEEXT_CREDENTIAL_PAIR0_ structure


## -description


The <b>IKEEXT_CREDENTIAL_PAIR0</b> structure is  used to store credential information used for the authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CREDENTIAL_PAIR0</b> is the specific implementation of IKEEXT_CREDENTIAL_PAIR used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7, <a href="https://msdn.microsoft.com/fe18503d-fd1c-45b6-86c7-9b452036f8c8">IKEEXT_CREDENTIAL_PAIR1</a> is available. For Windows 8, <a href="https://msdn.microsoft.com/013b7b6c-aee6-40f3-b8c4-ef98784165ca">IKEEXT_CREDENTIAL_PAIR2</a> is available.</div><div> </div>

## -struct-fields




### -field localCredentials

Local credentials used for authentication.

See <a href="https://msdn.microsoft.com/cb5aa4b6-71e7-43d4-a69c-4f209cd9755b">IKEEXT_CREDENTIAL0</a> for more information.


### -field peerCredentials

Peer credentials used for authentication.

See <a href="https://msdn.microsoft.com/cb5aa4b6-71e7-43d4-a69c-4f209cd9755b">IKEEXT_CREDENTIAL0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/cb5aa4b6-71e7-43d4-a69c-4f209cd9755b">IKEEXT_CREDENTIAL0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

