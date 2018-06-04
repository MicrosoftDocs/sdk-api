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

# CInstance::Commit


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Commit</b> method returns the current instance to WMI.


## -parameters






## -returns



Use the <b>SUCCEEDED</b> or <b>FAILED</b> macro on the returned <b>HRESULT</b> to determine success or failure of the method.




## -remarks



If the client cancels the query, the <b>Commit</b> method returns an error. A provider writer can use this fact to terminate an enumeration.

Also, framework providers should call this method to commit rather than <a href="https://msdn.microsoft.com/619adf78-26db-4a90-90ba-bdacb3e55975">Provider::Commit</a>.  <b>Provider::Commit</b> calls <b>CInstance::Release</b> automatically. Smart <a href="https://msdn.microsoft.com/aed29340-eb64-437d-b7e8-4f0e49c8288a">CInstance</a> pointers cannot be used in this case because the smart <b>CInstance</b> pointer would call <b>CInstance::Release</b> in its destructor. If the release has already occurred, an exception will result. Issues of this type are best resolved by allowing the <b>CInstance</b> instance, or a smart pointer to it, to call <b>CInstance::Release</b> when it is appropriate.



