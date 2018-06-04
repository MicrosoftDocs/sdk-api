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

# ShellWindowFindWindowOptions enumeration


## -description



            Specifies options for finding window in the Shell windows collection.
        


## -enum-fields




### -field SWFO_NEEDDISPATCH


            The window must have an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. 
            


### -field SWFO_INCLUDEPENDING


            Include windows that were registered with <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>.
            


### -field SWFO_COOKIEPASSED


            Causes <a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">IShellWindows::FindWindowSW</a> to interpret <i>pvarLoc</i>  as a cookie rather than a PIDL.
            


## -see-also




<a href="https://msdn.microsoft.com/e609c8b6-2b2e-4188-894c-5c85960206ea">IShellWindows</a>



<a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">IShellWindows::FindWindowSW</a>
 

 

