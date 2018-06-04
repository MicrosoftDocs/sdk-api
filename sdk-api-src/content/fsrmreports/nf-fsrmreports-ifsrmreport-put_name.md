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

# IFsrmReport::put_Name


## -description


Retrieves or sets the name of the report.

This property is read/write.


## -parameters


## -remarks



If not set, FSRM generates a unique name for you.

The name is used in the report.  If email notification is sent, the subject contains the report name.


#### Examples

For an example, see 
     <a href="https://msdn.microsoft.com/2dd5420b-33ab-4831-83b8-a9a4b2201a60">Adding a Report to a Job</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2172a543-b3b7-453e-887b-05c8ee74f197">IFsrmReport</a>
 

 

