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

# IUserNotification2::Show


## -description


Displays the user information in a balloon-style tooltip.


## -parameters




### -param pqc [in, optional]

Type: <b><a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a>*</b>

An <a href="https://msdn.microsoft.com/94dee6cc-a142-4180-a562-14f4ded16884">IQueryContinue</a> interface pointer, used to determine whether the notification display can continue or should stop (for example, if the user closes the notification). This value can be <b>NULL</b>.


### -param dwContinuePollInterval [in]

Type: <b>DWORD</b>

The length of time, in milliseconds, to display user information.


### -param pSink [in]

Type: <b><a href="https://msdn.microsoft.com/f746a4d4-8649-43a1-ac9b-773402dfb6c7">IUserNotificationCallback</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/f746a4d4-8649-43a1-ac9b-773402dfb6c7">IUserNotificationCallback</a> interface, used to handle mouse click and hover actions on the notification area icon and within the notification itself. This value can be <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6605a014-4f79-4856-8fd9-df926ea76052">IUserNotification2</a>



<a href="https://msdn.microsoft.com/1f908581-9635-4090-9e52-1dfb9a206d38">Show</a>
 

 

