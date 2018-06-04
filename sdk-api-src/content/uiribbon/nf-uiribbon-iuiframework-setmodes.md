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

# IUIFramework::SetModes


## -description



			Specifies the application modes to enable. 
		


## -parameters




### -param iModes

Type: <b>INT32</b>


					A bit mask that identifies the modes. 
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




				A mode indicates the functionality required and, therefore, which elements should be displayed (or 
				hidden) at run time, depending on the state or context of an application. For example, network connectivity 
				may directly impact the functionality of an application and require a "Network" mode of 
				network-related commands whenever a connection is detected.
			


				Modes are specified for elements in the Ribbon markup and bound to individual controls at run time.
			


				Modes can be applied to a Ribbon <a href="https://msdn.microsoft.com/2e73a89c-4d31-4075-93c8-e43213a20791">Tab</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn934674">Group</a>. 
				

<div class="alert"><b>Note</b>  
				Modes can be applied to <a href="https://msdn.microsoft.com/library/windows/hardware/ff545233">Button</a>, <a href="https://msdn.microsoft.com/dece1100-ed04-49a3-a16d-3c5d5e7a2225">SplitButton</a>, and <a href="https://msdn.microsoft.com/41031be2-43bc-4f75-b37a-1dcecc1635e1">DropDownButton</a> controls when hosted in the left 
				column of the Application Menu. 
				</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>



<a href="https://msdn.microsoft.com/70d7c357-8614-4883-97ae-6fce4fe7dcc4">Markup Elements</a>



<a href="https://msdn.microsoft.com/8e9d85c5-33e4-4212-b9e4-2fc3b492c273">Reconfiguring the Ribbon with Application Modes</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

