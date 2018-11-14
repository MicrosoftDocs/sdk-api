---
UID: NF:fwpmu.FwpmEngineClose0
title: FwpmEngineClose0 function
author: windows-sdk-content
description: Closes a session to a filter engine.
old-location: fwp\fwpmengineclose0_func.htm
tech.root: fwp
ms.assetid: e96165a8-95ad-4cb0-9f45-e8af22f83a52
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: FwpmEngineClose0, FwpmEngineClose0 function [Filtering], fwp.fwpmengineclose0_func, fwpmu/FwpmEngineClose0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - FwpmEngineClose0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FwpmEngineClose0
: 
---

# FwpmEngineClose0 function


## -description


The <b>FwpmEngineClose0</b> function closes a session to a filter engine.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The session was closed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



After an application has completed adding or removing system objects, it may call the <b>FwpmEngineClose0</b> function to close the open session to the filter engine.

A filter engine session is also closed when a client process terminates.

If this function is called with a transaction in progress, the transaction will be aborted.

<b>FwpmEngineClose0</b> is a specific implementation of FwpmEngineClose. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=98331">Kernel-Mode FwpmEngineClose0</a>
 

 

