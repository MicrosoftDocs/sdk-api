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

# DdeFreeDataHandle function


## -description


Frees a Dynamic Data Exchange (DDE) object and deletes the data handle associated with the object. 


## -parameters




### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object to be freed. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a> function or returned by the <a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application must call <b>DdeFreeDataHandle</b> under the following circumstances: 

<ul>
<li>To free a DDE object that the application allocated by calling the <a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a> function if the object's data handle was never passed by the application to another Dynamic Data Exchange Management Library (DDEML) function </li>
<li>To free a DDE object that the application allocated by specifying the <b>HDATA_APPOWNED</b> flag in a call to <a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>
</li>
<li>To free a DDE object whose handle the application received from the <a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a> function </li>
</ul>
The system automatically frees an unowned object when its handle is returned by a DDE callback function or is used as a parameter in a DDEML function. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/7695d435-3bb4-4041-8992-9155efa8911e">DdeAccessData</a>



<a href="https://msdn.microsoft.com/024655dd-f4de-4aad-a6fe-81e8322e228e">DdeClientTransaction</a>



<a href="https://msdn.microsoft.com/4ef31f93-5fb5-400e-9c87-60d99785aae7">DdeCreateDataHandle</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

