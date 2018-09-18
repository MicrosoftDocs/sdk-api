---
UID: NF:mstask.ITaskScheduler.SetTargetComputer
title: ITaskScheduler::SetTargetComputer
author: windows-sdk-content
description: The SetTargetComputer method selects the computer that the ITaskScheduler interface operates on, allowing remote task management and enumeration.
old-location: taskschd\itaskscheduler_settargetcomputer.htm
tech.root: taskschd
ms.assetid: e56d2384-026e-44e0-b6b7-20a41a421e09
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: ITaskScheduler interface [Task Scheduler],SetTargetComputer method, ITaskScheduler.SetTargetComputer, ITaskScheduler::SetTargetComputer, SetTargetComputer, SetTargetComputer method [Task Scheduler], SetTargetComputer method [Task Scheduler],ITaskScheduler interface, _msb_itaskscheduler_settargetcomputer, mstask/ITaskScheduler::SetTargetComputer, taskschd.itaskscheduler_settargetcomputer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskScheduler.SetTargetComputer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskScheduler::SetTargetComputer


## -description


<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="https://msdn.microsoft.com/67ed58e1-e54c-4c02-a6c4-d9ab8dc0f83e">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>SetTargetComputer</b> method selects the computer that the 
<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a> interface operates on, allowing remote task management and enumeration.


## -parameters




### -param pwszComputer [in]

A pointer to a <b>null</b>-terminated wide character string that specifies the target computer name for the current instance of the 
<b>ITaskScheduler</b> interface. Specify the target computer name in the Universal Naming Convention (UNC) format. To indicate the local computer, set this value to <b>NULL</b> or to the local computer's UNC name.

<div class="alert"><b>Note</b>  When specifying a remote computer name, use two backslash (\\) characters before the computer name. For example, use "\\ComputerName" instead of "ComputerName".</div>
<div> </div>

## -returns



The 
<b>SetTargetComputer</b> method returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_SERVICE_NOT_INSTALLED</b></dt>
</dl>
</td>
<td width="60%">
The Task Scheduler service is not installed on the target computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwszComputer</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -remarks



For a Windows Server 2003, Windows XP computer to create, monitor, or control tasks on a Windows Vista computer, the following operations should be completed on the Windows Vista computer, and the user who is calling the <b>ITaskScheduler::SetTargetComputer</b> method must be a member of the Administrators group on the remote Windows Vista  computer.<p class="proch"><img alt="" src="../common/wedge.gif"/><b>Enable the "Share File and Printers" exception in Windows Firewall</b>

<ol>
<li>Click Start, and then click Control Panel.</li>
<li>In Control Panel, click <b>Classic View</b> and then double-click the <b>Windows Firewall </b> icon.</li>
<li>In the Windows Firewall window, click the <b>Exceptions</b> tab and select <b>File and Printer Sharing exception</b> check box.</li>
</ol>
<p class="proch"><img alt="" src="../common/wedge.gif"/><b>Enable the "Remote Registry" service</b>

<ul>
<li>Open a Command Prompt window and enter the following command: <b>net start "Remote Registry"</b></li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/70c276e1-a45a-4a7d-aacc-3eb647675098">ITaskScheduler</a>
 

 

