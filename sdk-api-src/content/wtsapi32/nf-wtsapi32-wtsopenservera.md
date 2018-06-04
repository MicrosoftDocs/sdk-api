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

# WTSOpenServerA function


## -description


Opens a handle to the specified Remote Desktop Session Host (RD Session Host) server.


## -parameters




### -param pServerName [in]

Pointer to a null-terminated string specifying the NetBIOS name of the RD Session Host server.


## -returns



If the function succeeds, the return value is a handle to the specified server.

If the function fails, it returns a handle that is not valid. You can test the validity of the handle by using it in another function call.




## -remarks



When you have finished using the handle returned by 
<b>WTSOpenServer</b>, release it by calling the <a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a> function.

You do not need to open a handle for operations performed on the RD Session Host server on which your application is running. Use the constant <b>WTS_CURRENT_SERVER_HANDLE</b> instead.




## -see-also




<a href="https://msdn.microsoft.com/092a6107-21bf-40a7-9fe7-f069eb0c89ca">WTSCloseServer</a>
 

 

