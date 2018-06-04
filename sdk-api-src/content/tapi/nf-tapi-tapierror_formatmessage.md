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

# TAPIERROR_FORMATMESSAGE macro


## -description


The 
<b>TAPIERROR_FORMATMESSAGE</b> macro generates an identifier for standard TAPI error codes that can be used in the <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> function.


## -parameters




#### - ErrCode

TAPI error code.


## -remarks



This mechanism should be used only for displaying information on errors for which the application has no defined method of recovery (that is, unexpected or internal errors). In most cases (unlike the following simplified example), it is desirable to include additional text informing the user of actions the application takes (or the user should take) as a result of the unhandled error.

If the application gets an error result from any TAPI function, the error value can be passed to the 
<b>TAPIERROR_FORMATMESSAGE</b> macro, which generates the message identifier to be passed to <b>FormatMessage</b>. 


#### Examples

The following example uses <b>FormatMessage</b> to produce an error string that corresponds to a TAPI error code.

<pre class="syntax" xml:space="preserve"><code>lResult = lineClose(hLine);

if (lResult &lt; 0)
{
    FormatMessage(FORMAT_MESSAGE_FROM_HMODULE,
                  (LPCVOID)GetModuleHandle("TAPIUI.DLL"),
                  TAPIERROR_FORMATMESSAGE(lResult),
                  0,
                  (LPTSTR)pBuf,
                  BUFSIZE,
                  NULL);
    MessageBox(hWnd,pBuf,"TAPI ERROR",MB_OK);
}</code></pre>


