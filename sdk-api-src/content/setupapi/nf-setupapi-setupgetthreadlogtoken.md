---
UID: NF:setupapi.SetupGetThreadLogToken
title: SetupGetThreadLogToken function
author: windows-sdk-content
description: The SetupGetThreadLogToken function retrieves the log token for the thread from which this function was called.
old-location: devinst\setupgetthreadlogtoken.htm
old-project: devinst
ms.assetid: a4d870d0-2a1a-4319-9e52-e5bf469c4cdf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SetupGetThreadLogToken, SetupGetThreadLogToken function [Device and Driver Installation], devinst.setupgetthreadlogtoken, setupapi/SetupGetThreadLogToken, setupapilog-ref_2d342787-8c0e-4198-85cc-e64d51e98abb.xml
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
tech.root: 
req.typenames: TSSD_ConnectionPoint, *PTSSD_ConnectionPoint
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.lib
 - Setupapi.dll
 - Ext-MS-Win-setupapi-logging-l1-1-0.dll
 - setupapi.dll
api_name:
 - SetupGetThreadLogToken
product: Windows
targetos: Windows
req.lib: Setupapi.lib
req.dll: 
req.irql: 
req.product: ADAM
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
 

 

