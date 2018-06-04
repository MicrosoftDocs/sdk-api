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

# _WLX_TERMINAL_SERVICES_DATA structure


## -description


<p class="CCE_Message">[The WLX_TERMINAL_SERVICES_DATA structure is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>WLX_TERMINAL_SERVICES_DATA</b> structure is used to provide <a href="https://msdn.microsoft.com/c9567a5b-bd56-4ae1-9eac-af0bb5a6842a">GINA</a> with Terminal Services user configuration information.

The structure is populated by the 
<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a> function.


## -struct-fields




### -field ProfilePath

Terminal Services profile path, overrides the standard profile path.


### -field HomeDir

Terminal Services home directory, overrides standard home directory.


### -field HomeDirDrive

Terminal Services home directory drive, overrides the standard drive.


## -remarks



The Terminal Services user configuration information is received from the Domain Controller and SAM database.




## -see-also




<a href="https://msdn.microsoft.com/a7b81d76-74de-44a8-92ad-765ad1f7013e">WlxQueryTerminalServicesData</a>
 

 

