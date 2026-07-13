---
UID: NF:roerrorapi.IsErrorPropagationEnabled
title: IsErrorPropagationEnabled function
description: Indicates whether the CoreApplication.UnhandledErrorDetected event occurs for the errors that are returned by the delegate registered as a callback function for a Windows Runtime API event or the completion of an asynchronous method.
helpviewer_keywords: ["IsErrorPropagationEnabled","IsErrorPropagationEnabled function [Windows Runtime]","roerrorapi/IsErrorPropagationEnabled","winrt.iserrorpropagationenabled"]
old-location: winrt\iserrorpropagationenabled.htm
tech.root: WinRT
ms.assetid: 9F2DBD9C-5562-43F1-B3C4-475BB0000364
ms.date: 12/5/2018
ms.keywords: IsErrorPropagationEnabled, IsErrorPropagationEnabled function [Windows Runtime], roerrorapi/IsErrorPropagationEnabled, winrt.iserrorpropagationenabled
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: RuntimeObject.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IsErrorPropagationEnabled
 - roerrorapi/IsErrorPropagationEnabled
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RuntimeObject.lib
 - RuntimeObject.dll
 - API-MS-Win-Core-WinRT-error-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-WinRT-error-l1-1-1.dll
api_name:
 - IsErrorPropagationEnabled
---

# IsErrorPropagationEnabled function


## -description

<div class="alert"><b>Note</b>  This function is deprecated.  Going forward, all Windows 8.1 and Windows 10 apps  can operate automatically as if error propagation is enabled, and do not need to check dynamically whether error propagation is enabled. </div><div> </div>Indicates whether the <a href="https://msdn.microsoft.com/863a06ac-b8ec-440a-8445-1dbbf1b04263">CoreApplication.UnhandledErrorDetected</a> event occurs for the errors that are returned by the delegate registered as a callback function for a Windows Runtime API event or the completion of an asynchronous method.



## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <a href="https://msdn.microsoft.com/863a06ac-b8ec-440a-8445-1dbbf1b04263">CoreApplication.UnhandledErrorDetected</a> event occurs for the errors that are returned by the delegate registered as a callback function for a Windows Runtime API event or the completion of an asynchronous method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
Indicates  that the <a href="https://msdn.microsoft.com/863a06ac-b8ec-440a-8445-1dbbf1b04263">CoreApplication.UnhandledErrorDetected</a> event does not occur for the errors that are returned by the delegate registered as a callback function for a Windows Runtime API event or the completion of an asynchronous method.
                

</td>
</tr>
</table>

## -remarks

For Windows 8 apps, this value is <b>FALSE</b>, and errors returned by a delegate registered as a callback function    for the asynchronous completion of a Windows Runtime API or for a Windows Runtime API event are ignored. For Windows 8.1 and Windows 10 apps, this value is <b>TRUE</b>, and errors from callback functions that return control to operating system code are propagated to the global error handler.

Use this function only when your code needs to interoperate with both Windows 8 and newer applications by using the same binary.

## -see-also

<a href="https://msdn.microsoft.com/863a06ac-b8ec-440a-8445-1dbbf1b04263">CoreApplication.UnhandledErrorDetected</a>

