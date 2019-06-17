---
UID: NF:setupapi.SetupSetThreadLogToken
title: SetupSetThreadLogToken function (setupapi.h)
author: windows-sdk-content
description: The SetupSetThreadLogToken function sets the log context, as represented by a log token, for the thread from which this function was called.
old-location: devinst\setupsetthreadlogtoken.htm
tech.root: devinst
ms.assetid: c5295bb8-73c8-4516-91fe-ba11aa8a0657
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: SetupSetThreadLogToken, SetupSetThreadLogToken function [Device and Driver Installation], devinst.setupsetthreadlogtoken, setupapi/SetupSetThreadLogToken, setupapilog-ref_0247f1a0-3c40-45dc-8162-a3b5e09d76e4.xml
ms.topic: function
f1_keywords: ["setupapi/SetupSetThreadLogToken"]
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupSetThreadLogToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SetupSetThreadLogToken function


## -description


The <b>SetupSetThreadLogToken</b> function sets the log context, as represented by a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">log token</a><u>,</u> for the thread from which this function was called. A subsequent call to <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a> made within the same thread retrieves the log token that was most recently set for the thread.


## -parameters




### -param LogToken [in]

A <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">log token</a> that is either a system-defined log token or was returned by <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a>.


## -returns



None




## -remarks



<b>SetupSetThreadLogToken</b> establishes a log context for the thread from which the function was called. The log context is represented by a <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">log token</a>, which can be retrieved by calling <a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a>. 

For more information about log tokens, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="https://docs.microsoft.com/windows-hardware/drivers/install/setting-and-getting-a-log-token-for-a-thread">Setting and Getting a Log Token for a Thread</a>.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/install/log-tokens">Log Tokens</a>



<a href="https://docs.microsoft.com/windows-hardware/drivers/install/setting-and-getting-a-log-token-for-a-thread">Setting and Getting a Log Token for a Thread</a>



<a href="https://docs.microsoft.com/windows/desktop/api/setupapi/nf-setupapi-setupgetthreadlogtoken">SetupGetThreadLogToken</a>
 

 

