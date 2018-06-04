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

# IFaxLoggingOptions interface


## -description


The <b>IFaxLoggingOptions</b> interface is used by a fax client application to access and configure the event logging categories and the activity logging options that the fax service is using.

The <b>IFaxLoggingOptions</b> interface is accessed through an <a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a> interface. It provides access to the <a href="https://msdn.microsoft.com/225afdb8-7249-4aa5-bbde-638adf02eb41">FaxActivityLogging</a> and <a href="https://msdn.microsoft.com/c46f1b55-8211-4c9b-a622-356f2ea2db36">FaxEventLogging</a> methods. 


## -remarks



To create a <b>FaxLoggingOptions</b> object in C++, call the <a href="https://msdn.microsoft.com/51abefd8-e8b2-42f8-a4dc-f2aa8ffc9ef6">LoggingOptions</a> method.




## -see-also




<a href="https://msdn.microsoft.com/438e4e89-88c9-431d-b774-98e65cf57064">FaxLoggingOptions</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9e8718b9-f957-43c4-92de-f320aa42a096">IFaxServer</a>
 

 

