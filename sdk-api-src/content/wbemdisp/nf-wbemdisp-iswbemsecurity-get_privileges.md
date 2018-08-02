---
UID: NF:wbemdisp.ISWbemSecurity.get_Privileges
title: ISWbemSecurity::get_Privileges
author: windows-sdk-content
description: The Privileges property is an SWbemPrivilegeSet object. This property is used to enable or disable specific Windows privileges. You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.
old-location: wmi\swbemsecurity_privileges.htm
old-project: WmiSdk
ms.assetid: 6e4cae22-23d6-4981-b38c-d298654e59ab
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemSecurity interface [Windows Management Instrumentation],Privileges property, ISWbemSecurity.get_Privileges, ISWbemSecurity::get_Privileges, Privileges property [Windows Management Instrumentation], Privileges property [Windows Management Instrumentation],ISWbemSecurity interface, Privileges property [Windows Management Instrumentation],SWbemSecurity object, SWbemSecurity object [Windows Management Instrumentation],Privileges property, SWbemSecurity.Privileges, _hmm_swbemsecurity.privileges, get_Privileges, wmi.swbemsecurity_privileges
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
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
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemSecurity.Privileges
 - ISWbemSecurity.Privileges
 - ISWbemSecurity.get_Privileges
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemSecurity::get_Privileges


## -description


The 
<b>Privileges</b> property is an 
<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a> object. This property is used to enable or disable specific Windows privileges. You may need to set one of these privileges to perform specific tasks using the Windows Management Instrumentation (WMI) API.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



This setting allows you to grant or revoke privileges as part of a WMI moniker string. For the complete list of applicable values, see <a href="https://msdn.microsoft.com/235a1115-d8c4-4334-a4e0-fc539da4d2ae">WbemPrivilegeEnum</a> and <a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>.

You can change the privileges defined for the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>, 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>, 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>, and 
<a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SwbemLocator</a> objects by adding 
<a href="https://msdn.microsoft.com/18ee4587-6347-4075-b5e9-c5fb02f3cbf7">SWbemPrivilege</a> objects to the 
<b>Privileges</b> property.

There are fundamental differences in how different versions of Windows handle changes to privileges. If you are developing an application that is only used on Windows platforms, you can set or revoke privileges at any time.

The following example sets the <b>SeDebugPrivilege</b> on the initial moniker connection to obtain an <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate, (Debug)}")</pre>
</td>
</tr>
</table></span></div>
For more information about how to format the security string for a moniker connection, see <a href="https://msdn.microsoft.com/f9400597-81bb-44a8-80dc-aba0160aea26">Privilege Constants</a>.

The following example performs the same task, but it sets the privilege after the initial log on to WMI.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set Service = GetObject( _
    "winmgmts:{impersonationLevel=impersonate}")
Service.Security_.Privileges.AddAsString "SeDebugPrivilege", True</pre>
</td>
</tr>
</table></span></div>
Note that for calls to <a href="https://msdn.microsoft.com/729ed4e3-2c5c-4bb4-acc6-cf9ad0d5eaf1">SwbemPrivilegeSet.AddAsString</a>, you must use the full name of the security privilege, for example, "SeDebugPrivilege" instead of "Debug".




## -see-also




<a href="https://msdn.microsoft.com/11bb8723-f329-4083-8219-2256ce44a5e3">Executing Privileged Operations</a>



<a href="https://msdn.microsoft.com/073cf2d4-f7ee-45a6-8fa6-ca77a4870346">SWbemPrivilegeSet</a>



<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a>
 

 

