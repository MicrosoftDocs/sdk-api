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

# MI_Instance_Normalize function


## -description


Parses an <a href="https://msdn.microsoft.com/E703D978-7B4B-4AB4-AB69-C9489F5AD58B">MI_Instance_ExFT</a> structure and 
    then retrieves  the <a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a> function 
    table.


## -parameters




### -param self [in, out]

A pointer to the object that receives the function table.


## -returns



A value of the <a href="https://msdn.microsoft.com/9AA2B479-E8A5-4F0C-A8A4-06DB7CB7CA2F">MI_Result</a> enumeration that specifies the 
      function return code. This can be one of the following codes.




## -see-also




<a href="https://msdn.microsoft.com/9B9C2BEF-02E8-4C7D-96DB-236BF6F9B1F9">MI Interfaces</a>



<a href="https://msdn.microsoft.com/3dce1817-7995-49e5-8cc0-ee9496665e5c">MI_Instance</a>



<a href="https://msdn.microsoft.com/a8cd93b7-c9e0-415e-811a-33826e38417f">MI_InstanceFT</a>
 

 

