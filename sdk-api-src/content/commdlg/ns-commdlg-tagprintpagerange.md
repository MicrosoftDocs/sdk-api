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

# tagPRINTPAGERANGE structure


## -description


Represents a range of pages in a print job. A print job can have more than one page range. This information is supplied in the <a href="https://msdn.microsoft.com/e843d2fc-d122-4112-bfc9-9bfb26e865da">PRINTDLGEX</a> structure when calling the <a href="https://msdn.microsoft.com/b7863533-9b97-4921-9d9c-3490958bfc81">PrintDlgEx</a> function.


## -struct-fields




### -field nFromPage

Type: <b>DWORD</b>

The first page of the range. 


### -field nToPage

Type: <b>DWORD</b>

The last page of the range. 


## -see-also




<a href="https://msdn.microsoft.com/28573019-f0bd-4a8e-a1a1-48559f658a81">Common Dialog Box Library</a>
 

 

