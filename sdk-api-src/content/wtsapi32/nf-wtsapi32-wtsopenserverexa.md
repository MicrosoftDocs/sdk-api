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

# WTSOpenServerExA function


## -description


Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server or Remote Desktop Virtualization Host (RD Virtualization Host) server.


## -parameters




### -param pServerName [in]

A pointer to a null-terminated string that contains the NetBIOS name of the server.


## -returns



If the function succeeds, the return value is a handle to the specified server.

If the function fails, it returns an invalid handle. You can test the validity of the handle by using it in another function call.




## -remarks



If the server specified by the <i>pServerName</i> parameter is an RD Session Host server, the behavior of this function is identical to  that of the <a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a> function.

To work with sessions running on virtual machines on the RD Virtualization Host server on which the calling application is running, specify <b>WTS_CURRENT_SERVER_NAME</b> for the <i>pServerName</i> parameter.

When you have finished using the handle returned by this function, release it by calling the <a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a> function.




## -see-also




<a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a>



<a href="https://msdn.microsoft.com/f0b7dce7-59eb-41b8-9a61-65a69d1cc1f3">WTSOpenServer</a>
 

 

