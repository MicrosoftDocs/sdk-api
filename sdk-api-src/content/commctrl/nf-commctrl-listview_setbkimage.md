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

# ListView_SetBkImage macro


## -description


Sets the background image in a list-view control. You can use this macro or send the <a href="https://msdn.microsoft.com/8fdd363c-ac12-498b-80b7-aaa5741cfd76">LVM_SETBKIMAGE</a> message explicitly.


## -parameters




### -param hwnd

TBD


### -param plvbki

Type: <b>LPLVBKIMAGE</b>

A pointer to an <a href="https://msdn.microsoft.com/d8b35356-d112-43e5-b1ad-7fb945c84e33">LVBKIMAGE</a> structure that contains the new background image information. 


#### - hwndLV

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to the list-view control. 


## -remarks



Because the list-view control uses OLE COM to manipulate the background images, the calling application must call <a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a> or <a href="https://msdn.microsoft.com/9a13e7a0-f2e2-466b-98f5-38d5972fa391">OleInitialize</a> before using this macro. It is best to call one of these functions when the application is initialized and call either <a href="https://msdn.microsoft.com/9411cbed-fa3b-46f7-b677-6ada53324edc">CoUninitialize</a> or <a href="https://msdn.microsoft.com/b2a8233f-7e1b-4c54-9363-7478c40c3830">OleUninitialize</a> when the application is terminating. 




## -see-also




<a href="https://msdn.microsoft.com/292750e5-add2-44e7-8fa9-8cc13eb2dbc8">ListView_GetBkImage</a>
 

 

