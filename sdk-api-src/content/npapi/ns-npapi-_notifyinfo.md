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

# _NOTIFYINFO structure


## -description


The <b>NOTIFYINFO</b> structure contains status information about a network connect or disconnect operation. It is used by the 
<a href="https://msdn.microsoft.com/a061b088-81ca-4276-a0d6-9f1d1282a039">AddConnectNotify</a> and 
<a href="https://msdn.microsoft.com/94bd969d-f94d-449c-971d-d17fff2c07e1">CancelConnectNotify</a> functions.


## -struct-fields




### -field dwNotifyStatus

This will be either NOTIFY_PRE or NOTIFY_POST to indicate whether this notification is sent before or after the connection or disconnection is performed.


### -field dwOperationStatus

This is set to WN_SUCCESS when <b>dwNotifyStatus</b> is NOTIFY_PRE. 




If <b>dwNotifyStatus</b> is set to NOTIFY_POST, <b>dwOperationStatus</b> contains the return status code from the function performing the operation: 
<a href="https://msdn.microsoft.com/37a3988c-18ee-400a-85c3-cc3cbdf015ea">NPAddConnection</a> or 
<a href="https://msdn.microsoft.com/e06768b2-760c-48f1-a6a4-896c3ea286f6">NPCancelConnection</a>.


### -field lpContext

Used by the application receiving the notification in order to keep a context for the operation between the pre-notification and the post-notification calls. In other words, it enables the notification application to match the advance notification call to the corresponding after-the-fact notification call for a particular event. The <b>lpContext</b> member is a <b>NULL</b> pointer when the notification function is called for advance notification. The notification function can return with <b>lpContext</b> still <b>NULL</b>, indicating that it is not interested in further notification for this specific operation. In this case, the notification function will not be called again with after-the-fact notification for this operation. If the advance notification function call returns a non-<b>NULL</b> value in <b>lpContext</b>, this value is passed in when the notification function is called for the after-the-fact notification for that same operation.

