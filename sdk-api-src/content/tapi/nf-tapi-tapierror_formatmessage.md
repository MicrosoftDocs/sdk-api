---
UID: NF:tapi.TAPIERROR_FORMATMESSAGE
title: TAPIERROR_FORMATMESSAGE macro
author: windows-sdk-content
description: The TAPIERROR_FORMATMESSAGE macro generates an identifier for standard TAPI error codes that can be used in the FormatMessage function.
old-location: tapi2\tapierror_formatmessage.htm
tech.root: Tapi
ms.assetid: 95817592-467f-438e-ae81-b4c2fff42d1f
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: TAPIERROR_FORMATMESSAGE, TAPIERROR_FORMATMESSAGE macro [TAPI 2.2], _tapi2_tapierror_formatmessage, tapi/TAPIERROR_FORMATMESSAGE, tapi2.tapierror_formatmessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: macro
req.header: tapi.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - TAPIERROR_FORMATMESSAGE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


