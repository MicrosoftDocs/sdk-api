---
UID: NF:wbemdisp.ISWbemServices.ExecMethod
title: ISWbemServices::ExecMethod
author: windows-sdk-content
description: Executes a method that is exported by a method provider.
old-location: wmi\swbemservices_execmethod.htm
old-project: WmiSdk
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ExecMethod, ExecMethod method [Windows Management Instrumentation], ExecMethod method [Windows Management Instrumentation],ISWbemServices interface, ExecMethod method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],ExecMethod method, ISWbemServices.ExecMethod, ISWbemServices::ExecMethod, SWbemServices object [Windows Management Instrumentation],ExecMethod method, SWbemServices.ExecMethod, _hmm_swbemservices.execmethod, wmi.swbemservices_execmethod
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemServices.ExecMethod
 - ISWbemServices.ExecMethod
 - ISWbemServices.ExecMethod
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ExecMethod


## -description


The 
<b>ExecMethod</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object executes a method that is exported by a method provider. This method blocks while the method that is forwarded to the appropriate provider executes. The information and status are then returned. The provider, rather than WMI, implements the method.

This method is called in the synchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strObjectPath

Required. String that contains the object path of the object for which the method is executed. For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param strMethodName

Required. Name of the method for the object.


### -param objWbemInParameters




### -param iFlags [optional]

Reserved. This value must be zero.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemOutParameters






#### - objWbemInParams [optional]

An 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains the input parameters for the method being executed. By default, this parameter is undefined. For more information, see 
<a href="https://msdn.microsoft.com/be9332b5-8094-44a2-8632-af9957ecf36b">Constructing InParameters Objects and Parsing OutParameters Objects</a>.


## -returns



If the method is successful, an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object is returned. The returned object contains the out parameters and return value for the method that is being executed.




## -remarks



Use <b>SWbemServices.ExecMethod</b> as an alternative to direct access for executing a <a href="gloss_p.htm">provider method</a> in cases where it is not possible to execute a method directly. The 
<b>ExecMethod</b> method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters. Otherwise, the recommended means of invoking a method is to use direct access. For more information, see 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>.

For example, the following code example that calls the 
<a href="https://msdn.microsoft.com/b7a815a2-7bf6-436f-b3b4-de55eeb2de0e">StartService</a> provider method in <a href="https://msdn.microsoft.com/713402d3-ee73-4a6c-afb9-ad8033a4c580">Win32_Service</a> uses direct access.

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
This example calls <b>SWbemServices.ExecMethod</b> to execute the <a href="https://msdn.microsoft.com/b7a815a2-7bf6-436f-b3b4-de55eeb2de0e">StartService</a> method. Note that an object path is required because <b>SWbemServices.ExecMethod</b> is not operating on the object already, unlike 
<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"</pre>
</td>
</tr>
</table></span></div>
The <b>SWbemServices.ExecMethod</b> method requires an object path. If the script already holds an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object, use the 
<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod</a> method.


#### Examples

The following example shows the 
<b>ExecMethod</b> method. The script creates a 
<a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> object that  represents a process that is running Notepad. It shows the setting up of an 
<a href="https://msdn.microsoft.com/fba1bb97-29f9-41d3-8ecc-f283989118c1">InParameters</a> object and how to obtain results from an 
<a href="https://msdn.microsoft.com/ae7774f7-8a53-44e4-a110-2aef9ae4037f">OutParameters</a> object. For a script that shows the same operations performed asynchronously, see 
<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">SWbemServices.ExecMethodAsync</a>. For an example of using direct access, see 
<a href="https://msdn.microsoft.com/be80abec-fab4-4403-bc29-d0d4a38e3c87">Create Method in Class Win32_Process</a>. For an example of the same operation using an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, see 
<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            &amp; " but had error " _
            &amp; "0x" &amp; hex(oOutParams.ReturnValue)
    End If
End If</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9c692bc7-246b-4619-a371-cc9e0e2d5a6e">Calling a Provider Method</a>



<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>



<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod_</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

