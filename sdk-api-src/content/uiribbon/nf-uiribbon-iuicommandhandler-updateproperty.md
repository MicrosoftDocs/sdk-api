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

# IUICommandHandler::UpdateProperty


## -description



			Responds to property update requests from the Windows Ribbon framework.
		


## -parameters




### -param commandId [in]

Type: <b>UINT32</b>


					The ID for the Command, which is specified in the Markup resource file.
				


### -param key [in]

Type: <b>REFPROPERTYKEY</b>


					The <a href="https://msdn.microsoft.com/12bc7fda-ff69-4316-8baf-cc97e19a231c">Property Key</a> to update.
				


### -param currentValue [in, optional]

Type: <b>const PROPVARIANT*</b>


					A pointer to the current value for <i>key</i>. This parameter can be <b>NULL</b>.
				


### -param newValue [out]

Type: <b>PROPVARIANT*</b>


					When this method returns, contains a pointer to the new value for 
					<i>key</i>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




			This method should be allowed to return before any subsequent calls to the Ribbon framework are made.

The values of Command properties, such as <a href="https://msdn.microsoft.com/bb75487c-a222-4d92-87cb-1c11d137af7b">UI_PKEY_Enabled</a> or <a href="https://msdn.microsoft.com/4d704133-bba7-4c32-a552-d748b66455eb">UI_PKEY_Label</a>, are set through calls to <a href="https://msdn.microsoft.com/d04071d1-f3f2-4327-bf4c-6348dec4e2f1">SetUICommandProperty</a> or <a href="https://msdn.microsoft.com/6f6f6815-5523-42d9-a6b2-a21dd26756c0">InvalidateUICommand</a>.




## -see-also




<a href="https://msdn.microsoft.com/cd739f99-b3f2-4ddb-a844-eb888d9c7f67">IUICommandHandler</a>



<a href="https://msdn.microsoft.com/79d092c9-347b-4b8f-8ba4-a8f696ce6a85">Windows Ribbon Framework Samples</a>
 

 

