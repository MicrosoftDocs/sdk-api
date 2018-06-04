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

# IPrintDocumentPackageStatusEvent::PackageStatusUpdated


## -description


Updates the status of the package when the  print job in progress raises an event, or the job completes.


## -parameters




### -param packageStatus [in]

The status update.


## -returns



If the <b>PackageStatusUpdated</b> method completes successfully, it returns an S_OK. Otherwise it returns an appropriate HRESULT  error code.




## -see-also




<a href="https://msdn.microsoft.com/A2178E6A-04AD-4024-A083-5C76A5F60743">IPrintDocumentPackageStatusEvent</a>



<a href="https://msdn.microsoft.com/A499CB8D-B2E3-4343-A9AF-079C75EF1441">PrintDocumentPackageStatus</a>
 

 

