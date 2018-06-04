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

# ILocator::get_Modulation


## -description



The <b>get_Modulation</b> method gets the modulation type.




## -parameters




### -param Modulation






#### - pModulation [out]

Receives the modulation type, as a member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff567735">ModulationType</a> enumeration.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



See <a href="https://msdn.microsoft.com/84a5b2ce-d26b-4ffc-b757-a799658f2b34">put_Modulation</a> for the definition of <b>ModulationType</b>.




## -see-also




<a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator Interface</a>
 

 

