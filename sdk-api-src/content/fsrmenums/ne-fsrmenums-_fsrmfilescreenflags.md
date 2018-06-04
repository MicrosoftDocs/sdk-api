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

# _FsrmFileScreenFlags enumeration


## -description


Defines the options for failing IO operations that violate a file screen.


## -enum-fields




### -field FsrmFileScreenFlags_Enforce

If this flag is set, the server will fail any IO operation that violates the file screen. If this flag is 
      not set, the server will not fail violating IO operations but will still run any action associated with the file 
      screen.


## -see-also




<a href="https://msdn.microsoft.com/af888368-36a8-401e-b4df-6b0cc0dfb422">IFsrmFileScreenBase::FileScreenFlags</a>
 

 

