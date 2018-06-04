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

# IFsrmClassificationManager::WaitForClassificationCompletion


## -description


<p class="CCE_Message">[This method is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a> class.]

Waits for the specified period of time or until classification has finished running.


## -parameters




### -param waitSeconds [in]

The number of seconds to wait for classification and the reports to complete. The method returns when the 
      period expires or classification and the reports complete. To wait indefinitely, set the value to 
      –1. The value must be in the range from  –1 through 2,147,483.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the reports completed; otherwise, 
      <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -remarks



To run the classification, call the 
    <a href="https://msdn.microsoft.com/50fdc5c8-d2eb-4206-b0fa-0de2696d29c7">IFsrmClassificationManager::RunClassification</a> 
    method.

After 
    <b>WaitForClassificationCompletion</b> 
    returns, access the 
    <a href="https://msdn.microsoft.com/02c62b7d-a128-432a-a15a-51de092b5bab">IFsrmClassificationManager.ClassificationLastError</a> 
    property to determine if the reports completed successfully.




## -see-also




<a href="https://msdn.microsoft.com/4a8e0426-792d-49d8-acf3-ab00480e24ac">FsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/cc504f6c-00d7-4f9d-9688-1c29b5066ce6">IFsrmClassificationManager</a>



<a href="https://msdn.microsoft.com/f0a10671-9383-4935-b773-31f047732e27">IFsrmClassificationManager.ClassificationRunningStatus</a>



<a href="https://msdn.microsoft.com/6ff821e3-f0bd-4c66-8ced-edbbfbc8503b">IFsrmClassificationManager2</a>



<a href="https://msdn.microsoft.com/79571ae1-726e-491b-b41e-6cd10cdf3936">MSFT_FSRMClassification</a>
 

 

