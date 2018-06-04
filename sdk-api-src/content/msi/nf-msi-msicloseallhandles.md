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

# MsiCloseAllHandles function


## -description


The 
<b>MsiCloseAllHandles</b> function closes all open installation handles allocated by the current thread. This is a diagnostic function and should not be used for cleanup.


## -parameters






## -returns



This function returns 0 if all handles are closed. Otherwise, the function returns the number of handles open prior to its call.




## -remarks



<b>MsiCloseAllHandles</b> only closes handles allocated by the calling thread, and does not affect handles allocated by other threads, such as the install handle passed to custom actions.

The 
<a href="https://msdn.microsoft.com/1227493a-58dc-4e41-b6d7-9ecce0b3df40">MsiOpenPackage</a> function opens a handle to a package and the 
<a href="https://msdn.microsoft.com/fdc5a2f5-c44a-4cb3-b206-a598bd60024b">MsiOpenProduct</a> function opens a handle to a product. These function are for use with functions that access the product database.




## -see-also




<a href="https://msdn.microsoft.com/05a16915-6b47-4d51-b62a-5a4d92b87e50">Handle Management Functions</a>
 

 

