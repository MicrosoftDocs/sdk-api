---
UID: NF:setupapi.SetupGetThreadLogToken
title: SetupGetThreadLogToken function (setupapi.h)
description: The SetupGetThreadLogToken function retrieves the log token for the thread from which this function was called.
helpviewer_keywords: ["SetupGetThreadLogToken","SetupGetThreadLogToken function [Device and Driver Installation]","devinst.setupgetthreadlogtoken","setupapi/SetupGetThreadLogToken","setupapilog-ref_2d342787-8c0e-4198-85cc-e64d51e98abb.xml"]
old-location: devinst\setupgetthreadlogtoken.htm
tech.root: devinst
ms.assetid: a4d870d0-2a1a-4319-9e52-e5bf469c4cdf
ms.date: 12/05/2018
ms.keywords: SetupGetThreadLogToken, SetupGetThreadLogToken function [Device and Driver Installation], devinst.setupgetthreadlogtoken, setupapi/SetupGetThreadLogToken, setupapilog-ref_2d342787-8c0e-4198-85cc-e64d51e98abb.xml
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupGetThreadLogToken
 - setupapi/SetupGetThreadLogToken
dev_langs:
 - c++
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
req.apiset: ext-ms-win-setupapi-logging-l1-1-0 (introduced in Windows 8)
---

# SetupGetThreadLogToken function


## -description

The <b>SetupGetThreadLogToken</b> function retrieves the <a href="/windows-hardware/drivers/install/log-tokens">log token</a> for the thread from which this function was called.



## -returns

<b>SetupGetThreadLogToken</b> returns the log token for the thread from which the function was called. If a log token is not set for the thread, <b>SetupGetThreadLogToken</b> returns the system-defined log token LOGTOKEN_UNSPECIFIED.

## -remarks

To set a log token for a thread, call <a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetthreadlogtoken">SetupSetThreadLogToken</a>. 

For more information about log tokens, see <a href="/windows-hardware/drivers/install/log-tokens">Log Tokens</a>.

For more information about using log tokens, see <a href="/windows-hardware/drivers/install/setting-and-getting-a-log-token-for-a-thread">Setting and Getting a Log Token for a Thread</a>.

## -see-also

<a href="/windows-hardware/drivers/install/log-tokens">Log Tokens</a>



<a href="/windows-hardware/drivers/install/setting-and-getting-a-log-token-for-a-thread">Setting and Getting a Log Token for a Thread</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupsetthreadlogtoken">SetupSetThreadLogToken</a>
