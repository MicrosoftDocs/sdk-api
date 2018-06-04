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

# IUICommandHandler::Execute


## -description


Responds to execute events on Commands bound to the Command handler.  


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>


					The ID for the Command, which is specified in the Markup resource file.
				


### -param verb [in]

Type: <b><a href="https://msdn.microsoft.com/cce26367-9915-4e95-9362-1e32eb9ff034">UI_EXECUTIONVERB</a></b>


					The <a href="https://msdn.microsoft.com/cce26367-9915-4e95-9362-1e32eb9ff034">UI_EXECUTIONVERB</a> or action that is initiated by the user.
				


### -param key [in, optional]

Type: <b>const PROPERTYKEY*</b>


					A pointer to a <a href="https://msdn.microsoft.com/12bc7fda-ff69-4316-8baf-cc97e19a231c">Property Key</a> that has changed value. This parameter can be <b>NULL</b>.
				


### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>


					A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.
				


### -param commandExecutionProperties [in, optional]

Type: <b><a href="https://msdn.microsoft.com/599c4cdf-6c91-473c-904f-b264391c94ed">IUISimplePropertySet</a>*</b>


					A pointer to an <a href="https://msdn.microsoft.com/599c4cdf-6c91-473c-904f-b264391c94ed">IUISimplePropertySet</a> object that contains 
					Command state properties and property values, such as screen coordinates and list item indices. This parameter can be <b>NULL</b>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each Command in a View must be bound to a new or existing Command handler in the host application.




## -see-also




<a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

