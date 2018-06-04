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

# IWMReaderAdvanced2::GetSaveAsProgress


## -description



The <b>GetSaveAsProgress</b> method retrieves the percentage of data that has been saved.




## -parameters




### -param pdwPercent [out]

Pointer to a <b>DWORD</b> containing the percentage of data that has been saved.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method must only be called after <a href="https://msdn.microsoft.com/97bdac1f-8830-45c0-9229-322ad72b3954">IWMReaderAdvanced2::SaveFileAs</a> has been called.

When saving a file, the operation can take some time. This call must be made between the events WMT_SAVEAS_START and WMT_SAVEAS_STOP. If it is called before WMT_SAVEAS_START, or there is an error, this method returns zero. It returns 100 following a successful WMT_SAVEAS_STOP event.




## -see-also




<a href="https://msdn.microsoft.com/5d741e49-9fdf-4f8d-9ea1-faaecf879be4">IWMReaderAdvanced2 Interface</a>
 

 

