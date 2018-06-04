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

# IUPnPDeviceDocumentAccessEx::GetDocument


## -description


The <b>GetDocument</b> method retrieves the XML device description document for a UPnP device.


## -parameters




### -param pbstrDocument






#### - [out, retval]

Receives the XML device description document for the device.

After obtaining the XML device document, the memory for this parameter must be free by passing it to SysFreeString.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



<div class="alert"><b>Note</b>  This method does not support scripting.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/9ea79bbb-3841-4704-9606-56fcd2f8bf89">IUPnPDeviceDocumentAccessEx</a>
 

 

