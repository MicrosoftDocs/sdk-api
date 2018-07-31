---
UID: NF:wbemdisp.ISWbemObject.ExecMethod_
title: ISWbemObject::ExecMethod_
author: windows-sdk-content
description: The ExecMethod_ method of the SWbemObject object executes a method exported by a method provider.
old-location: wmi\swbemobject_execmethod_.htm
old-project: WmiSdk
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ExecMethod_, ExecMethod_ method [Windows Management Instrumentation], ExecMethod_ method [Windows Management Instrumentation],ISWbemObject interface, ExecMethod_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],ExecMethod_ method, ISWbemObject.ExecMethod_, ISWbemObject::ExecMethod_, SWbemObject object [Windows Management Instrumentation],ExecMethod_ method, SWbemObject.ExecMethod_, _hmm_swbemobject.execmethod_, wmi.swbemobject_execmethod_
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
 - SWbemObject.ExecMethod_
 - ISWbemObject.ExecMethod_
 - ISWbemObject.ExecMethod_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::ExecMethod_


## -description


The 
<b>ExecMethod_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object executes a method exported by a method provider.

This method pauses while the method that is forwarded to the appropriate provider executes. The information and status are then returned. The provider rather than WMI implements the method.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strMethodName [in]

Required. Name of the method for the object.


### -param objWbemInParameters




### -param iFlags [in, optional]

Reserved and must be set to 0 (zero) if specified.


### -param objWbemNamedValueSet




### -param objWbemOutParameters






#### - objwbemInParams [in, optional]

This is an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains the input parameters for the method being executed. By default, this parameter is undefined. For more information, see 
<a href="https://msdn.microsoft.com/be9332b5-8094-44a2-8632-af9957ecf36b">Constructing InParameters Objects and Parsing OutParameters Objects</a>.


#### - objwbemNamedValueSet [in, optional]

Typically, it is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If this method is successful, an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns. The returned object contains the out parameters and return value for the method being executed.




## -remarks



This method is similar to 
<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a>, but it operates directly on the object whose method is to be executed. For example, the following code example calls the 
<a href="https://msdn.microsoft.com/b7a815a2-7bf6-436f-b3b4-de55eeb2de0e">StartService</a> provider method in <a href="https://msdn.microsoft.com/713402d3-ee73-4a6c-afb9-ad8033a4c580">Win32_Service</a> and uses 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">direct access</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()</pre>
</td>
</tr>
</table></span></div>
This version calls <b>SWbemObject.ExecMethod_</b> to execute the <a href="https://msdn.microsoft.com/b7a815a2-7bf6-436f-b3b4-de55eeb2de0e">StartService</a> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")</pre>
</td>
</tr>
</table></span></div>
Use <b>SWbemObject.ExecMethod_</b> as an alternative to direct access for executing a <a href="gloss_p.htm">provider method</a> in cases where it is not possible to execute a method directly. For example, you would use <b>SWbemObject.ExecMethod_</b> with a scripting language that does not support output parameters if your method has out parameters. Otherwise, the recommended means of invoking a method is to use direct access.

<ul>
<li>The <b>SWbemObject.ExecMethod_</b> method assumes the object represented by <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> contains the method to execute. By contrast, <a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a> requires an object path. Use <b>SWbemObject.ExecMethod_</b> if you already have obtained the object whose method you want to execute.</li>
</ul>

#### Examples

The following example shows the 
<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">ExecMethod</a> method.The script creates a 
<a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> object representing a process running Notepad. For more information about a script illustrating the same operations performed asynchronously, see 
<a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">SWbemObject.ExecMethodAsync_</a>. For an example using direct access, see 
<a href="https://msdn.microsoft.com/be80abec-fab4-4403-bc29-d0d4a38e3c87">Create Method in Class Win32_Process</a> . For an example of the same operation using an <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object, see 
<b>SWbemServices.ExecMethod</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            &amp; "0x" &amp; hex(oOutParams.ReturnValue)
    End If
End If</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">SWbemObject.ExecMethodAsync_</a>



<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a>
 

 

