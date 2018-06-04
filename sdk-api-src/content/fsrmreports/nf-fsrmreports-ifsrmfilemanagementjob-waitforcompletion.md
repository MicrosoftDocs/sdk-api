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

# IFsrmFileManagementJob::WaitForCompletion


## -description


<p class="CCE_Message">[This property is supported for compatibility but it's recommended to use the 
    <a href="https://msdn.microsoft.com/1CE772FA-CE33-4900-A499-058175A7C37E">FSRM WMI Classes</a> to manage FSRM. Please see the 
    <a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a> class.]

Waits for the specified period of time or until the job has finished running.


## -parameters




### -param waitSeconds [in]

The number of seconds to wait for the job to complete. The method returns when the period expires or the 
      job complete. To wait indefinitely, set the value to –1.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the job completed; otherwise, 
      <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -remarks



To run the job, call the 
    <a href="https://msdn.microsoft.com/2db27e05-5c3b-4827-a616-36fd46281911">IFsrmFileManagementJob::Run</a> method. Jobs run 
     asynchronously, calling this method blocks your thread until the job completes or the timeout period 
     expires.

After <b>WaitForCompletion</b> 
     returns, access the 
     <a href="https://msdn.microsoft.com/f7a7d5fd-b060-41f6-be1f-038ab252259a">IFsrmFileManagementJob::LastError</a> 
     property to determine if the reports completed successfully.




## -see-also




<a href="https://msdn.microsoft.com/e9ae697d-4f7c-47d9-8d2a-c46c2e5f838f">IFsrmFileManagementJob</a>



<a href="https://msdn.microsoft.com/1ce33602-0ada-4d82-aebb-9dee7dc8b2f3">MSFT_FSRMFileManagementJob</a>
 

 

