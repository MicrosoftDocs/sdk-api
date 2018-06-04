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

# IGPMRSOP::CreateQueryResults


## -description


Executes a Resultant Set of Policy (RSoP) query. The method supports both logging mode and planning mode queries. Before calling this method, set the appropriate logging mode or planning mode properties. For more information and a list of properties, see 
<a href="https://msdn.microsoft.com/8a1b6a38-e2a6-455d-8d50-2545b7d6c5d2">IGPMRSOP Property Methods</a>. RSoP planning mode requires a domain controller running Windows Server to perform the query.


## -parameters






## -returns



<h3>JScript</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.

<h3>VB</h3>
Returns <b>S_OK</b> if successful. Returns a failure code if an error occurs.




## -remarks



Call the 
<a href="https://msdn.microsoft.com/c2bf9050-4db0-4bf0-a063-0076ba191ff6">IGPMRSOP::ReleaseQueryResults</a> method to release the WMI namespace created by this method.

In the GPMC UI, logging mode is also referred to as "Group Policy Results", and planning mode is also referred to as "Group Policy Modeling".




## -see-also




<a href="https://msdn.microsoft.com/86bbb143-2a9c-4fda-ba13-4f0fd09b2cd3">IGPMRSOP</a>
 

 

