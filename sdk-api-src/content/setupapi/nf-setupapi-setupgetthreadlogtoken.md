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

# SetupGetThreadLogToken function


## -description


The <b>SetupGetThreadLogToken</b> function retrieves the <a href="devinst.log_tokens">log token</a> for the thread from which this function was called.


## -parameters






## -returns



<b>SetupGetThreadLogToken</b> returns the log token for the thread from which the function was called. If a log token is not set for the thread, <b>SetupGetThreadLogToken</b> returns the system-defined log token LOGTOKEN_UNSPECIFIED.




## -remarks



To set a log token for a thread, call <a href="https://msdn.microsoft.com/library/windows/hardware/ff552216">SetupSetThreadLogToken</a>. 

For more information about log tokens, see <a href="devinst.log_tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="devinst.setting_and_getting_a_log_token_for_a_thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="devinst.log_tokens">Log Tokens</a>



<a href="devinst.setting_and_getting_a_log_token_for_a_thread">Setting and Getting a Log Token for a Thread</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff552216">SetupSetThreadLogToken</a>
 

 

