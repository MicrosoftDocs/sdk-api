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

# IAssocHandler::IsRecommended


## -description


Indicates whether the application is registered as a recommended handler for the queried file type.


## -parameters






## -returns



Type: <b>HRESULT</b>

Returns S_OK if the program is recommended; otherwise, S_FALSE.




## -remarks



Applications that register themselves as handlers for particular file types can specify whether they are recommended handlers. This has no effect on the actual behavior of the applications when launched. It is simply provided as a hint to the user and a value that the UI can utilize programmatically, if desired. For example, the Shell's <b>Open With</b> dialog separates entries into <b>Recommended Programs</b> and <b>Other Programs</b>.

Note that program recommendations may change over time. One example is provided when the user chooses an application from the <b>Other Programs</b> of the <b>Open With</b> dialog to open a particular file type. That may cause the Shell to "promote" that application to recommended status for that file type. Because the recommended status may change over time, applications should not cache this value, but query it each time it is needed.

If <a href="https://msdn.microsoft.com/83db466b-e00c-4015-879f-c5c222f45b8c">SHAssocEnumHandlers</a> was called with the ASSOC_FILTER_RECOMMENDED flag, then only recommended handlers are returned. If the ASSOC_FILTER_NONE flag was used, then you must call <b>IAssocHandler::IsRecommended</b> on each <a href="https://msdn.microsoft.com/5d5a107c-2c0e-4242-8f40-97421937167c">IAssocHandler</a> object to determine whether it is recommended or not.



