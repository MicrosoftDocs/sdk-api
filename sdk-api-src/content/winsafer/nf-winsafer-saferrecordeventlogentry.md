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

# SaferRecordEventLogEntry function


## -description


The <b>SaferRecordEventLogEntry</b> function saves messages to an event log.


## -parameters




### -param hLevel [in]

SAFER_LEVEL_HANDLE that contains the details of the rule to send to the event log.


### -param szTargetPath [in]

Path of the file that attempted to run.


### -param lpReserved

Reserved for future use. This parameter should be set to <b>NULL</b>.


## -returns



<b>TRUE</b> if the function succeeds; otherwise, <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If <a href="https://msdn.microsoft.com/f82c4f40-5c37-4f97-95a2-4b2cc26bf41e">SaferIdentifyLevel</a> returns a SAFER_LEVEL_HANDLE with a LevelId that is anything other than SAFER_LEVELID_FULLYTRUSTED (0x40000), <b>SaferRecordEventLogEntry</b> can be called to facilitate troubleshooting. For example, clicking a button in excel.exe might attempt to launch another process that is not fully trusted. This might display an obscure error message because the program remapped the error returned from CreateProcess. To ease troubleshooting, some Safer functions call <b>SaferRecordEventLogEntry</b> to send an event to the event log.



