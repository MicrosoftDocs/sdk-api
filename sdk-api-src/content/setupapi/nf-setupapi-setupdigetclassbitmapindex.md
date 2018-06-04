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

# SetupDiGetClassBitmapIndex function


## -description


The <b>SetupDiGetClassBitmapIndex</b> function retrieves the index of the mini-icon supplied for the specified class.


## -parameters




### -param ClassGuid [in, optional]

A pointer to the GUID of the <a href="https://msdn.microsoft.com/en-us/library/windows/hardware/ff552344">device setup class</a> for which to retrieve the mini-icon. This pointer is optional and can be <b>NULL</b>.


### -param MiniIconIndex [out]

A pointer to a variable of type INT that receives the index of the mini-icon for the specified device setup class. If the <i>ClassGuid</i> parameter is <b>NULL</b> or if there is no mini-icon for the specified class, <b>SetupDiGetClassBitmapIndex</b> returns the index of the mini-icon for the Unknown device setup class. 


## -returns



If there is a min-icon for the specified device setup class, <b>SetupDiGetClassBitmapIndex</b> returns <b>TRUE</b>. Otherwise, this function returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a>. If the <i>ClassGuid</i> parameter is <b>NULL</b>, or if there is no mini-icon for the specified class, the function returns <b>FALSE</b> and <a href="http://go.microsoft.com/fwlink/p/?linkid=169416">GetLastError</a> returns ERROR_NO_DEVICE_ICON.




## -remarks



For a list of the device setup class mini-icons and their corresponding indexes, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff551005">SetupDiDrawMiniIcon</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551005">SetupDiDrawMiniIcon</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552053">SetupDiLoadClassIcon</a>
 

 

