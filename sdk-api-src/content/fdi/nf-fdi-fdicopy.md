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

# FDICopy function


## -description


The <b>FDICopy</b> function extracts files from cabinets.


## -parameters




### -param hfdi [in]

A valid FDI context handle returned by the <a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a> function.


### -param pszCabinet [in]

The name of the cabinet file, excluding any path information, from which to extract files. If a file is split over multiple cabinets, <b>FDICopy</b>  allows for subsequent cabinets to be opened.


### -param pszCabPath [in]

The pathname of the cabinet file, but not including the name of the file itself. For example, "C:\MyCabs\". 

The contents of <i>pszCabinet</i> are appended to <i>pszCabPath</i> to create the full pathname of the cabinet.


### -param flags [in]

No flags are currently defined and this parameter should be set to zero.


### -param pfnfdin [in]

Pointer to an application-defined callback notification function to update the application on the status of the decoder. The function should be declared using the <a href="https://msdn.microsoft.com/7655ddb2-7cd4-4012-913c-9909fcea639a">FNFDINOTIFY</a> macro.


### -param pfnfdid [in]

Not currently used by FDI. This parameter should be set to <b>NULL</b>.


### -param pvUser [in, optional]

Pointer to an application-specified value to pass to the notification function.


## -returns



If the function succeeds, it returns <b>TRUE</b>; otherwise, <b>FALSE</b>.

Extended error information is provided in the <a href="https://msdn.microsoft.com/ddbccad9-a68c-4be7-90dc-e3dd25f5cf3b">ERF</a> structure used to create the FDI context.




## -see-also




<a href="https://msdn.microsoft.com/90634725-b7a8-4369-8a91-684debee9548">FDICreate</a>
 

 

