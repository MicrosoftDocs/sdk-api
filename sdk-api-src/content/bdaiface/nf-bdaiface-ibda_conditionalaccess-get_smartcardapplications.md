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

# IBDA_ConditionalAccess::get_SmartCardApplications


## -description


The <b>get_SmartCardApplications</b> method retrieves a list of the smart card applications.


## -parameters




### -param pulcApplications [in, out]


            Receives a count of the number of smart card applications in the <i>rgApplications</i> array.
          


### -param ulcApplicationsMax [in]


            The maximum number of smart card applications that the <i>rgApplications</i> buffer can hold.
          


### -param rgApplications [in, out]


            Pointer to a buffer that receives an array of smart card applications. Each array element is a <a href="https://msdn.microsoft.com/14d9cfbd-46c4-4be2-8631-f0916820c129">SmartCardApplication</a> structure.
          


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an error code.




## -remarks



<div class="alert"><b>Note</b>  The <i>pulcApplications</i> parameter is marked in the IDL file as [in, out] but is used as an [in] parameter. To preserve binary compatibility with previous versions, it has not been changed.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/93bd3c38-2591-4d36-b296-5ad939487277">IBDA_ConditionalAccess Interface</a>
 

 

