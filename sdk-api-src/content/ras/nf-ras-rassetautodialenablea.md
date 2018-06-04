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

# RasSetAutodialEnableA function


## -description


The 
<b>RasSetAutodialEnable</b> function enables or disables the AutoDial feature for a specified TAPI dialing location. For more information about TAPI dialing locations, see  <a href="_tapi3_telephony_application_programming_interfaces">Telephony Application Programming Interfaces (TAPI)</a>  in the Platform Software Development Kit (SDK).


## -parameters




### -param

TBD




#### - dwDialingLocation [in]

Specifies the identifier of a TAPI dialing location.


#### - fEnabled [in]

Specifies <b>TRUE</b> to enable AutoDial for the dialing location indicated by the <i>dwDialingLocation</i> parameter. Specifies <b>FALSE</b> to disable it.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a non-zero error code from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -see-also




<a href="https://msdn.microsoft.com/221f91e6-86bd-4450-92c8-ec3290712c18">RasGetAutodialEnable</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

