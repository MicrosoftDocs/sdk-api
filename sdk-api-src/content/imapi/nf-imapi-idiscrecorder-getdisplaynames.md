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

# IDiscRecorder::GetDisplayNames


## -description


Retrieves a formatted name for the recorder that can be displayed. The name consists of the manufacturer and product identifier of the device.


## -parameters




### -param pbstrVendorID [out]

Vendor of the disc recorder. This parameter can be <b>NULL</b>.


### -param pbstrProductID [out]

Product name of the disc recorder. This parameter can be <b>NULL</b>.


### -param pbstrRevision [out]

Revision of the disc recorder. This is typically the revision of the recorder firmware, but it can be a revision for the entire device. This parameter can be <b>NULL</b>.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -remarks



The display names are typically combined into a string that is displayed in recorder selection list boxes or other GUI components.

The combination of these three strings does not produce a unique identifier for this specific recorder. Combine these strings with the string returned from 
<a href="https://msdn.microsoft.com/library/windows/hardware/mt432961">GetPath</a> to create a unique value.




## -see-also




<a href="https://msdn.microsoft.com/fc861cbb-a14e-499e-8b80-f5912e4f6076">IDiscRecorder</a>
 

 

