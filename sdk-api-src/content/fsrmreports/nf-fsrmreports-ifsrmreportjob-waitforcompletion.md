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

# IFsrmReportJob::WaitForCompletion


## -description


Waits for the reports in the job to complete.


## -parameters




### -param waitSeconds [in]

The number of seconds to wait for the reports to complete. The method returns when the period expires or the reports complete. To wait indefinitely, set the value to –1.


### -param completed [out]

Is <b>VARIANT_TRUE</b> if the reports completed; otherwise, <b>VARIANT_FALSE</b>.


## -returns



The method returns the following return values.




## -remarks



To run the job, call the <a href="https://msdn.microsoft.com/74f369d1-2e3d-49a5-bf54-c1b7c13efbd7">IFsrmReportJob::Run</a> method.

After <b>WaitForCompletion</b> returns, access the <a href="https://msdn.microsoft.com/7a610d10-8e43-49b7-b85b-bb0ec122fda8">IFsrmReportJob::LastError</a> property to determine if the reports completed successfully.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/8087542d-5873-414b-8903-544c2e57cba1">Running a Report Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ea8a3f6b-326b-4c8f-a6fc-7b7525c5543f">IFsrmReportJob</a>



<a href="https://msdn.microsoft.com/74f369d1-2e3d-49a5-bf54-c1b7c13efbd7">IFsrmReportJob::Run</a>
 

 

