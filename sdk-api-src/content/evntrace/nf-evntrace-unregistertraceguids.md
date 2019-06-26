---
UID: NF:evntrace.UnregisterTraceGuids
title: UnregisterTraceGuids function (evntrace.h)
author: windows-sdk-content
description: The UnregisterTraceGuids function unregisters an event trace provider and its event trace classes.
old-location: etw\unregistertraceguids.htm
tech.root: ETW
ms.assetid: 1fa10f66-a78b-4f40-9518-72d48365246e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UnregisterTraceGuids, UnregisterTraceGuids function [ETW], _evt_unregistertraceguids, base.unregistertraceguids, etw.unregistertraceguids, evntrace/UnregisterTraceGuids
ms.topic: function
f1_keywords: 
 - "evntrace/UnregisterTraceGuids"
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
 - UnregisterTraceGuids
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnregisterTraceGuids function


## -description


The 
<b>UnregisterTraceGuids</b> function unregisters an event trace provider and its event trace classes. 
		


## -parameters




### -param RegistrationHandle [in]

Handle to the event trace provider, obtained from an earlier call to the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>RegistrationHandle</i> parameter does not specify the handle to a registered provider or is <b>NULL</b>. 



								
							

</td>
</tr>
</table>
 




## -remarks



Providers call this function.

The event trace provider must have been registered previously by calling the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>
 

 

