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

# IFaxJobStatus interface


## -description


The <b>IFaxJobStatus</b> interface is used for notifications and to hold the dynamic information of the job. Dynamic information is data that changes as a job progresses. This may include the current job status, the page that is currently being transmitted, and the number of attempts the fax service has made to transmit the job (retries). The fax service uses this object to notify a fax client application of job updates. For more information, see <a href="https://msdn.microsoft.com/fe3e67bc-f9e5-4391-84f6-9960211b6df9">Fax Job Status</a>.


## -remarks



You do not create the <a href="https://msdn.microsoft.com/b4e2dc9e-6a32-4fc7-94fc-2132dedcec9e">FaxJobStatus</a> object. It is received as part of a notification when you implement <a href="https://msdn.microsoft.com/109f1f7d-f2e3-4db8-8800-3efa41b08942">IFaxServerNotify::OnIncomingJobChanged</a> or <a href="https://msdn.microsoft.com/132747ed-04b4-4803-976c-5274d8c9f73d">IFaxServerNotify::OnOutgoingJobChanged</a>, which include a parameter of the type <b>FaxJobStatus</b>. When the event occurs and the implemented function is called, you receive this object containing the dynamic information.




## -see-also




<a href="https://msdn.microsoft.com/b4e2dc9e-6a32-4fc7-94fc-2132dedcec9e">FaxJobStatus</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

