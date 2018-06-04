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

# IBDA_DRIDRMService::GetDRMStatus


## -description



      The GetDRMSTatus method returns the current status of the Digital Rights Management (DRM) system for a Media Transform Device (MTD) in a graph under the Protected Broadcast Device Architecture (PBDA). 


## -parameters




### -param pbstrDrmUuidList [out]

Address of a variable that gets a comma-delimited string of UUID values that identify the DRM systems supported by the MTD. This method allocates the memory for the variable by calling <b>SysAllocString</b> and returns the associated pointer in this parameter. The caller is memory and is responsible for deallocating it by calling <b>SysFreeString</b>.
          


### -param DrmUuid [out]


            Address of a variable that gets a GUID identifying the active DRM system for the MTD.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/9b04c960-a766-4322-bf18-e59176ee2ad1">IBDA_DRIDRMService</a>
 

 

