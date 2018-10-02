---
UID: NS:winsvc._SC_ACTION
title: "_SC_ACTION"
author: windows-sdk-content
description: Represents an action that the service control manager can perform.
old-location: base\sc_action_str.htm
tech.root: Services
ms.assetid: e2c355a6-affe-46bf-a3e6-f8c420422d46
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSC_ACTION, LPSC_ACTION, LPSC_ACTION structure pointer, SC_ACTION, SC_ACTION structure, SC_ACTION_NONE, SC_ACTION_REBOOT, SC_ACTION_RESTART, SC_ACTION_RUN_COMMAND, _SC_ACTION, _win32_sc_action_str, base.sc_action_str, winsvc/LPSC_ACTION, winsvc/SC_ACTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsvc.h
req.include-header: Windows.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winsvc.h
api_name:
 - SC_ACTION
product: Windows
targetos: Windows
req.typenames: SC_ACTION, *LPSC_ACTION
req.redist: 
---

# _SC_ACTION structure


## -description


Represents an action that the service control manager can perform.


## -struct-fields




### -field Type

The action to be performed. This member can be one of the following values from the <b>SC_ACTION_TYPE</b> enumeration type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SC_ACTION_NONE"></a><a id="sc_action_none"></a><dl>
<dt><b>SC_ACTION_NONE</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
No action.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_ACTION_REBOOT"></a><a id="sc_action_reboot"></a><dl>
<dt><b>SC_ACTION_REBOOT</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Reboot the computer.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_ACTION_RESTART"></a><a id="sc_action_restart"></a><dl>
<dt><b>SC_ACTION_RESTART</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Restart the service.

</td>
</tr>
<tr>
<td width="40%"><a id="SC_ACTION_RUN_COMMAND"></a><a id="sc_action_run_command"></a><dl>
<dt><b>SC_ACTION_RUN_COMMAND</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Run a command.

</td>
</tr>
</table>
 


### -field Delay

The time to wait before performing the specified action, in milliseconds.


## -remarks



This structure is used by the 
<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a> and 
<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a> functions, in the 
<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/180ca6d9-f2c3-4ea1-b2c6-319d08ef88ee">SERVICE_FAILURE_ACTIONS</a>
 

 

