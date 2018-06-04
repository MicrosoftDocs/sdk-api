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

# PropSheet_IdToIndex macro


## -description


Takes the resource identifier (ID) of a property sheet page and returns its zero-based index. You can use this macro or send the <a href="https://msdn.microsoft.com/91420c1e-7f8a-4b1c-a1fc-6ff65ee4b1b0">PSM_IDTOINDEX</a> message explicitly.


## -parameters




### -param hDlg

TBD


### -param id

TBD






#### - hPropSheetDlg

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle to the property sheet window.


#### - iPageID

Type: <b>int</b>

Resource ID of the page.


## -see-also




<a href="https://msdn.microsoft.com/358f9904-5b14-42e4-8095-f7b4d8144bc2">PropSheet_IndexToId</a>
 

 

