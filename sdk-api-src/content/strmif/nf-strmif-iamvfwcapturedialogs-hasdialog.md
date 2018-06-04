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

# IAMVfwCaptureDialogs::HasDialog


## -description



The <code>HasDialog</code> method determines if the specified dialog box exists in the driver.




## -parameters




### -param iDialog [in]

Desired dialog box. This is a member of the <a href="https://msdn.microsoft.com/0465d887-6452-4a67-9f52-a459620d12d2">VfwCaptureDialogs</a> enumeration.


## -returns



Returns S_OK if the driver contains the dialog box or S_FALSE otherwise.




## -remarks



This method calls the Video for Windows <b>videoDialog</b> function to query for the existence of the appropriate dialog box.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5198c80c-28f3-4b5c-9b3b-aa502bf3a384">IAMVfwCaptureDialogs Interface</a>
 

 

