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

# SetContractDelegateWindow function


## -description


Associates an app window other than the primary foreground window with an app's contracts. Use this function if you are a developer writing a Windows Store app in native C++.


## -parameters




### -param hwndSource [in]

Type: <b>HWND</b>

The handle of the app window normally associated with its contracts.


### -param hwndDelegate [in, optional]

Type: <b>HWND</b>

The handle of another of the app's windows that will act as the contract delegate for <i>hwndSource</i>. Set this value to <b>NULL</b> to remove the delegate connection.


## -returns



This function does not return a value.




## -remarks



This is an inline function, with the source code included in the header file. It is not included in a .lib or .dll file.




## -see-also




<a href="https://msdn.microsoft.com/89B23CB0-50CF-43BE-B397-542FA433018D">GetContractDelegateWindow</a>
 

 

