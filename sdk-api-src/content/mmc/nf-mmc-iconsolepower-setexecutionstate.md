---
UID: NF:mmc.IConsolePower.SetExecutionState
title: IConsolePower::SetExecutionState
author: windows-sdk-content
description: The SetExecutionState method sets the execution state for the current thread.
old-location: mmc\iconsolepower_setexecutionstate.htm
tech.root: mmc
ms.assetid: 1fbdc155-ea95-43b6-8aea-f47ff0c89859
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: ES_DISPLAY_REQUIRED, ES_SYSTEM_REQUIRED, IConsolePower interface [MMC],SetExecutionState method, IConsolePower.SetExecutionState, IConsolePower::SetExecutionState, SetExecutionState, SetExecutionState method [MMC], SetExecutionState method [MMC],IConsolePower interface, _slate_iconsolepower_setexecutionstate, mmc.iconsolepower_setexecutionstate, mmc/IConsolePower::SetExecutionState
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsolePower.SetExecutionState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsolePower::SetExecutionState


## -description


The 
<b>SetExecutionState</b> method sets the execution state for the current thread.


## -parameters




### -param dwAdd [in]

Flags to add to the snap-in execution state. This can be a combination of 0 or more of the following flags.



#### ES_DISPLAY_REQUIRED

The display (monitor) power-management requirement. If specified in <i>dwAdd</i>, the snap-in prohibits the operating system from invoking the power management routine for the display.



#### ES_SYSTEM_REQUIRED

The system power-management requirement. If specified in <i>dwAdd</i>, the snap-in prohibits the operating system from invoking the power management routine for the system.


### -param dwRemove [in]

Flags to remove from the snap-in's execution-state. This can be a combination of 0 or more of the preceding flags. Specifying one or more of the flags enables a snap-in to turn off a power management requirement established by an earlier call to 
<b>SetExecutionState</b>.

<div class="alert"><b>Note</b>  A power management requirement must be turned off before it can be turned on. An attempt to turn on a power management requirement without first turning it off returns an error <b>E_INVALIDARG</b>.</div>
<div> </div>

## -returns



If successful, the return value is <b>S_OK</b>. This method will return <b>S_FALSE</b> when invoked on a system that does not support power management. Other return values indicate an error code.




## -remarks



Call <b>IConsolePower::SetExecutionState</b> instead of 
<a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a>. Snap-ins must not call the <b>SetThreadExecutionState</b> function directly, doing so causes conflicts if multiple snap-ins are running on the same thread.

A snap-in defines its power requirements and sends them to MMC by calling 
<b>SetExecutionState</b>. After the snap-in calls 
<b>SetExecutionState</b>, its execution state remains in effect until the snap-in makes another call to 
<b>SetExecutionState</b>. Be aware that after <b>SetExecutionState</b> is called, the same instance of the <a href="https://msdn.microsoft.com/d34e8da0-2689-4514-be10-4c11008432b3">IConsolePower</a> interface must be used for subsequent calls to <b>SetExecutionState</b>. If a snap-in does not use the same instance of <b>IConsolePower</b>, then MMC cannot effectively call <a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a>. MMC maintains an array to track each snap-in's execution state, and calls <b>SetThreadExecutionState</b> for all snap-ins running on the thread.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;

// Specify that the display and system are required.
// pConsolePower was created previously by
// the CoCreateInstance method.
hr = pConsolePower-&gt;SetExecutionState(ES_DISPLAY_REQUIRED | ES_SYSTEM_REQUIRED,0);
switch (hr)
{
    case S_OK:
        OutputDebugString(_T("SetExecutionState: Succeeded\n"));
        break;

    case S_FALSE:
        // The system does not support power management.
        OutputDebugString(_T("SetExecutionState: Unsupported\n"));
        break;

    default:
        // Unexpected error occurred.
        OutputDebugString(_T("SetExecutionState: Failure\n"));
        break;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/83de4b7f-3214-4354-a4a0-721054e2e899">IConsolePower::ResetIdleTimer</a>



<a href="https://msdn.microsoft.com/9214ea84-7636-4a78-91fd-a5a5da8199a1">SetThreadExecutionState</a>
 

 

