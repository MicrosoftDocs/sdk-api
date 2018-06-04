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

# IFsrmPropertyBag::get_Messages


## -description


A list of the error messages that have been added to the bag.

This property is read-only.


## -parameters


## -remarks



The format of the message is 
    <i>module_name</i>,<i>rule_name</i>|<i>message</i> 
    (FSRM adds the <i>module_name</i>,<i>rule_name</i>| components to the 
    message that you specified when calling the 
    <a href="https://msdn.microsoft.com/2d9166fd-5211-4114-843f-2c6563941715">IFsrmPropertyBag::AddMessage</a> method).




## -see-also




<a href="https://msdn.microsoft.com/237f024d-2b1d-45d5-a63d-c530426278e6">IFsrmPropertyBag</a>



<a href="https://msdn.microsoft.com/2d9166fd-5211-4114-843f-2c6563941715">IFsrmPropertyBag::AddMessage</a>
 

 

