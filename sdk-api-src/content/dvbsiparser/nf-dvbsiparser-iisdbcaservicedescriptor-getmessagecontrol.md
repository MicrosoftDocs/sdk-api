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

# IIsdbCAServiceDescriptor::GetMessageControl


## -description


Gets the delay time, in days, before the automatic  entitlement management message (EMM) is displayed from a conditional access (CA) service descriptor.


## -parameters




### -param pbVal [out]

Receives the number of days before the EMM message is displayed. A value of 0xFF indicates that the delay time is
disabled (that the start of the delay time has been put on hold). 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When playing a previously received and stored program on a receiver with stored
reception functionality, a least significant bit of 1 in this field indicates that the
automatic display message will not be displayed.




## -see-also




<a href="https://msdn.microsoft.com/6d56e39d-3c7a-4c55-8d07-00e25eba18bd">IIsdbCAServiceDescriptor</a>
 

 

