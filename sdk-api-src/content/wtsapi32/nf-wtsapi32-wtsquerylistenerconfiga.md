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

# WTSQueryListenerConfigA function


## -description


Retrieves configuration information for a Remote Desktop Services listener.


## -parameters




### -param hServer [in]

A handle to an RD Session Host server. Always set this  parameter to <b>WTS_CURRENT_SERVER_HANDLE</b>.


### -param pReserved [in]

This parameter is reserved. Always set this parameter to <b>NULL</b>.


### -param Reserved [in]

This parameter is reserved. Always set this parameter to zero.


### -param pListenerName [in]

A pointer to a null-terminated string that contains the name of the listener to query.


### -param pBuffer [out]

A pointer to a <a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a> structure that receives the  retrieved listener configuration information.


## -returns



If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function.




## -remarks



This function does not retrieve the security descriptor for the listener. To retrieve the security descriptor, call the <a href="https://msdn.microsoft.com/6e49df9a-679d-4cc1-9297-90cf1e3509fa">WTSGetListenerSecurity</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6e49df9a-679d-4cc1-9297-90cf1e3509fa">WTSGetListenerSecurity</a>



<a href="https://msdn.microsoft.com/051cab0b-701c-4bb9-8728-6b383cdb8e6a">WTSLISTENERCONFIG</a>
 

 

