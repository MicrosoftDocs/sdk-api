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

# Provider::Flush


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/library/windows/hardware/hh406455">Provider</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>Flush</b> method is called by the provider framework to delete all unnecessary memory in use by the provider. Because your provider may be called again after a call to <b>Flush</b>, you must re-create any objects released by <b>Flush</b>. If you override this method, you should call the parent object's <b>Flush</b> method to release any framework memory associated with your provider.


## -parameters






## -returns



This method has no return values.




## -remarks



Override this method only if your framework provider allocates memory that can be flushed. If your provider chooses to override, include a call to <b>Provider::Flush</b> in the provider's implementation.

<div class="alert"><b>Note</b>  Because your provider may be called after a call to <b>Flush</b>, you must be prepared to re-create any items released by the call to <b>Flush</b>.</div>
<div> </div>


