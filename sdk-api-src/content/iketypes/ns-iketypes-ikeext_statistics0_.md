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

# IKEEXT_STATISTICS0_ structure


## -description



		The <b>IKEEXT_STATISTICS0</b> structure stores various IKE/AuthIP statistics.
<div class="alert"><b>Note</b>  <b>IKEEXT_STATISTICS0</b> is the specific implementation of IKEEXT_STATISTICS used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/73c36ea1-d009-4724-8b1c-54503ad57e4d">IKEEXT_STATISTICS1</a> is available.</div><div> </div>

## -struct-fields




### -field ikeStatistics

Statistics specific to IKE.

See <a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field authipStatistics

Statistics specific to AuthIP.

See <a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a> for more information.


### -field commonStatistics

Statistics common to IKE and AuthIP.

See <a href="https://msdn.microsoft.com/a53ef735-3223-4ff5-9b2a-d40ab0f53570">IKEEXT_COMMON_STATISTICS0</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/87dca500-bf57-463a-a6de-db270430ae29">IKEEXT_KEYMODULE_STATISTICS0</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

