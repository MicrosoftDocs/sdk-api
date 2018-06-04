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

# IWMReaderAdvanced2::SetPlayMode


## -description



The <b>SetPlayMode</b> method specifies the play mode.




## -parameters




### -param Mode [in]

Variable containing one member of the <a href="https://msdn.microsoft.com/da47fc9f-7762-4f92-8857-44a75a4cd00b">WMT_PLAY_MODE</a> enumeration type.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The default play mode is WMT_PLAY_MODE_AUTOSELECT, which enables the reader to pick the mode. If the application selects a play mode that is incompatible with the requested URL, an error is returned when the URL is opened. After the asynchronous reply to the <b>Open</b> request is completed, the mode is changed from WMT_PLAY_MODE_AUTOSELECT to the appropriately selected play mode. The play mode cannot be changed after the content has been opened, and returns an error if this is attempted.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>



<a href="https://msdn.microsoft.com/45c7e2c2-fff4-41a9-b5ce-76d8d6257e77">IWMReaderAdvanced2::GetPlayMode</a>
 

 

