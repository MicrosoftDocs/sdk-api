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

# IUIFramework::InvalidateUICommand


## -description



			Invalidates a Windows Ribbon framework Command property, value, or state. 
		


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>


					The ID for the Command, which is specified in the markup resource file.
				


### -param flags [in]

Type: <b><a href="https://msdn.microsoft.com/e3476cac-f088-46fd-bb4a-8a02e17461ed">UI_INVALIDATIONS</a></b>


					Identifies which <a href="https://msdn.microsoft.com/e3476cac-f088-46fd-bb4a-8a02e17461ed">aspect</a> of a command to invalidate.
					

<div class="alert"><b>Note</b>  
						Passing <b>UI_INVALIDATIONS_ALLPROPERTIES</b> invalidates all properties bound to a command, including value and state.
					</div>
<div> </div>

### -param key [in]

Type: <b>const PROPERTYKEY*</b>


					The property key of the command property or state.
				This parameter can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful; otherwise, an error value from the following list.
					

<table class="clsStd">
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>
					An invalid value for <i>key</i> was supplied.
				</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>
					The operation failed. 
					All the commands failed to invalidate, or none of the properties specified are supported.
				</td>
</tr>
</table>
 




## -remarks




				Resources defined in the Ribbon framework markup are stored in a resource table that is created 
				when the markup file is compiled into binary format. A resource cannot be reinstated from the Markup resource table after it has been invalidated.


				After invalidation, the framework queries the host application for the resource details. 
				
			

When a Command value is invalidated (<i>flags</i> contains UI_INVALIDATIONS_VALUE) the value of <i>key</i> is <b>NULL</b>.


				If <b>IUIFramework::InvalidateUICommand</b> is called multiple times
				and the <a href="https://msdn.microsoft.com/e3476cac-f088-46fd-bb4a-8a02e17461ed">UI_INVALIDATIONS</a> 
				value passed in each call specifies overlapping properties, such as <b>UI_INVALIDATIONS_STATE</b> 
				and <b>UI_INVALIDATIONS_ALLPROPERTIES</b>, then only one callback to the host application is created.
			




## -see-also




<a href="https://msdn.microsoft.com/a9b8a30d-dd00-4088-a588-304fde97b84e">IUIFramework</a>



<a href="https://msdn.microsoft.com/e3476cac-f088-46fd-bb4a-8a02e17461ed">UI_INVALIDATIONS</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

