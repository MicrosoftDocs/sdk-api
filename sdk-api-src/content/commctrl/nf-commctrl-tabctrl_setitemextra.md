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

# TabCtrl_SetItemExtra macro


## -description


Sets the number of bytes per tab reserved for application-defined data in a tab control. You can use this macro or send the <a href="https://msdn.microsoft.com/8315f1fd-8eca-48bd-bb4a-71b09e8aa2c4">TCM_SETITEMEXTRA</a> message explicitly. 


## -parameters




### -param hwndTC

TBD


### -param cb

Type: <b>int</b>

Number of extra bytes.


#### - hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the tab control. 


## -remarks



By default, the number of extra bytes is four. An application that changes the number of extra bytes cannot use the <a href="https://msdn.microsoft.com/e08c4528-5874-492c-97be-dfdf5f5636a9">TCITEM</a> structure to retrieve and set the application-defined data for a tab. Instead, you must define a new structure that consists of the <a href="https://msdn.microsoft.com/018a0de7-fc05-4b56-817b-1af36261fff2">TCITEMHEADER</a> structure followed by application-defined members. 

An application should only change the number of extra bytes when a tab control does not contain any tabs. 



