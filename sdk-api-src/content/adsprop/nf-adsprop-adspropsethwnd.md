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

# ADsPropSetHwnd function


## -description


The <b>ADsPropSetHwnd</b> function is used to notify the notification object of the property page window handle.


## -parameters




### -param hNotifyObj

TBD


### -param hPage [in]

A window handle of the property page.


#### - hNotifyObject [in]

The handle of the notification object. To obtain this handle, call <a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>.


## -returns



Returns zero if the notification object does not exist or nonzero otherwise.




## -remarks



An Active Directory Domain Services property sheet extension normally calls this function while processing the <a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a> message.

If the property sheet extension uses the <a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a> function, the extension should use <a href="https://msdn.microsoft.com/d0d26f32-1c15-4641-bdeb-0f464a510669">ADsPropSetHwndWithTitle</a> rather than <b>ADsPropSetHwnd</b>.




## -see-also




<a href="https://msdn.microsoft.com/bfca3801-0d24-4177-8173-b6bf4b854fae">ADsPropCreateNotifyObj</a>



<a href="https://msdn.microsoft.com/d0d26f32-1c15-4641-bdeb-0f464a510669">ADsPropSetHwndWithTitle</a>



<a href="https://msdn.microsoft.com/c7ed3d36-474e-4cb1-82aa-1e2c1ebd4b83">ADsPropShowErrorDialog</a>



<a href="_win32_wm_initdialog_cpp">WM_INITDIALOG</a>
 

 

