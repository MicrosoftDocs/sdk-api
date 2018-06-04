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

# GetSystemDEPPolicy function


## -description


Gets the data execution prevention (DEP) policy setting for the system.


## -parameters






## -returns



This function returns a value of type <b>DEP_SYSTEM_POLICY_TYPE</b>, which can be one of the following values.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AlwaysOff</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
DEP is disabled for all parts of the system, regardless of hardware support for DEP. The processor runs in PAE mode with 32-bit versions of Windows unless PAE is disabled in the boot configuration data. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AlwaysOn</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
DEP is enabled for all parts of the system. All processes always run with DEP enabled. DEP cannot be explicitly disabled for selected applications. System compatibility fixes are ignored. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OptIn</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
On systems with processors that are capable of hardware-enforced DEP, DEP is automatically enabled only for operating system components. This is the default setting for client versions of Windows. DEP can be explicitly enabled for selected applications or the current process. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OptOut</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
DEP is automatically enabled for operating system components and all processes. This is the default setting for Windows Server versions. DEP can be explicitly disabled for selected applications or the current process. System compatibility fixes for DEP are in effect. 

</td>
</tr>
</table>
 




## -remarks



The system-wide DEP policy is configured at boot time according to the policy setting in the boot configuration data.  To change the system-wide DEP policy setting, use the <a href="http://go.microsoft.com/fwlink/p/?linkid=93291">BCDEdit /set</a> command to set the <b>nx</b> boot entry option.

If the system DEP policy is OptIn or OptOut, DEP can be selectively enabled or disabled for the current process by calling the <a href="https://msdn.microsoft.com/17c9f522-fd64-4061-9212-8fc91cc96b18">SetProcessDEPPolicy</a> function. This function works only for 32-bit processes.

A user with administrative privileges can disable DEP for selected applications by using the <b>System</b> Control Panel application. If the system DEP policy is OptOut, DEP is disabled for these applications.

The Application Compatibility Toolkit can be used to create a list of individual applications that are exempt from DEP. If the system DEP policy is OptOut, DEP is automatically disabled for applications on the list. 




## -see-also




<a href="https://msdn.microsoft.com/75cd83a5-4b77-4ca9-b595-e32d0dd609d0">Data Execution Prevention</a>



<a href="https://msdn.microsoft.com/adf15b9c-24f4-49ea-9283-0db5f3f13e65">GetProcessDEPPolicy</a>



<a href="https://msdn.microsoft.com/82cb1d4e-c0e5-4601-aa55-9171a106c286">GetSystemDEPPolicy</a>
 

 

