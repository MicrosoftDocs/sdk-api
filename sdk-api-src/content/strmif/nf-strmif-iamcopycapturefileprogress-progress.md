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

# IAMCopyCaptureFileProgress::Progress


## -description



The <code>Progress</code> method is called periodically by the <a href="https://msdn.microsoft.com/d4084b12-b082-45c2-9f07-625b980c7e4c">ICaptureGraphBuilder2::CopyCaptureFile</a> method while it copies the file.




## -parameters




### -param iProgress [in]

Specifies the percentage of the copy operation that has completed, as a value between 0 and 100.


## -returns



Returns S_OK or an <b>HRESULT</b> error code.




## -remarks



Applications typically use the value of <i>iProgress</i> to update a progress bar on the user interface.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/780ffe63-f4b6-4b3c-b7a6-571b58aba4dd">IAMCopyCaptureFileProgress Interface</a>
 

 

