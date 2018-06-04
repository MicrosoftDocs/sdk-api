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

# _NOTIFYICONIDENTIFIER structure


## -description


Contains information used by <a href="https://msdn.microsoft.com/81ad13be-a908-4079-b47c-6f983919700b">Shell_NotifyIconGetRect</a> to identify the icon for which to retrieve the bounding rectangle.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of this structure, in bytes.


### -field hWnd

Type: <b>HWND</b>

A handle to the parent window used by the notification's callback function. For more information, see the <i>hWnd</i> member of the <a href="https://msdn.microsoft.com/fdcc42c1-b3e5-4b04-8d79-7b6c29699d53">NOTIFYICONDATA</a> structure.


### -field uID

Type: <b>UINT</b>

The application-defined identifier of the notification icon. Multiple icons can be associated with a single <i>hWnd</i>, each with their own <i>uID</i>.


### -field guidItem

Type: <b>GUID</b>

A registered GUID that identifies the icon. Use <b>GUID_NULL</b> if the icon is not identified by a GUID.


## -remarks



The icon can be identified to <a href="https://msdn.microsoft.com/81ad13be-a908-4079-b47c-6f983919700b">Shell_NotifyIconGetRect</a> through this structure in two ways:
            
                

<ul>
<li><i>guidItem</i> alone (recommended)</li>
<li><i>hWnd</i> plus <i>uID</i></li>
</ul>
If <i>guidItem</i> is not <b>GUID_NULL</b>, <i>hWnd</i> and <i>uID</i> are ignored.



