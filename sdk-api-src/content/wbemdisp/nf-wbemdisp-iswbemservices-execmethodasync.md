---
UID: NF:wbemdisp.ISWbemServices.ExecMethodAsync
title: ISWbemServices::ExecMethodAsync
author: windows-sdk-content
description: Executes a method that is exported by a method provider.
old-location: wmi\swbemservices_execmethodasync.htm
old-project: WmiSdk
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ExecMethodAsync, ExecMethodAsync method [Windows Management Instrumentation], ExecMethodAsync method [Windows Management Instrumentation],ISWbemServices interface, ExecMethodAsync method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],ExecMethodAsync method, ISWbemServices.ExecMethodAsync, ISWbemServices::ExecMethodAsync, SWbemServices object [Windows Management Instrumentation],ExecMethodAsync method, SWbemServices.ExecMethodAsync, _hmm_swbemservices.execmethodasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wmi.swbemservices_execmethodasync
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
 - SWbemServices.ExecMethodAsync
 - ISWbemServices.ExecMethodAsync
 - ISWbemServices.ExecMethodAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ExecMethodAsync


## -description


The 
<b>ExecMethodAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object executes a method that is exported by a method provider. The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes. Information and status are returned to the caller through events delivered to the sink that is specified in <i>objWbemSink</i>. The provider, rather than Windows Management Instrumentation (WMI), implements the method.

The method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For more information and an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink

Required. Create an <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects. Object sink that receives the result of the method call. The outbound parameters are sent to the <a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">SWbemSink.OnObjectReady</a> event of the supplied object sink. The results of the call mechanism are sent to the <a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">SWbemSink.OnCompleted</a> event of the supplied object sink. Be aware that <b>SWbemSink.OnCompleted</b> does not receive the return code of the WMI method. However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons. The result code that is returned from the WMI method is returned in the outbound parameter object supplied to <b>SWbemSink.OnObjectReady</b>. If any error code is returned, then the supplied <a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> object is not used. If the call is successful, then the user's <b>IWbemObjectSink</b> implementation is called to indicate the result of the operation.


### -param strObjectPath

Required. A string that contains the object path of the object for which the method is executed. For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param strMethodName

Required. The name of the method to execute.


### -param objWbemInParameters




### -param iFlags [optional]

Integer that determines the behavior of the call. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemAsyncContext [optional]

A 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/61f401d9-c874-472d-8dd3-7cf9d7f20a12">Making an Asynchronous Call with VBScript</a>.


#### - objWbemInParams [optional]

An 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains the input parameters for the method that is executed. By default, this parameter is undefined. For more information, see 
<a href="https://msdn.microsoft.com/be9332b5-8094-44a2-8632-af9957ecf36b">Constructing InParameters Objects and Parsing OutParameters Objects</a>.


## -returns



This method does not return a value. If the call is successful, an 
<a href="https://msdn.microsoft.com/ae7774f7-8a53-44e4-a110-2aef9ae4037f">OutParameters</a> object, which is also an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> is supplied to the sink that is specified in <i>objWbemSink</i>. The returned <b>OutParameters</b> object contains the output parameters and return value for the method being executed. For more information, see 
<a href="https://msdn.microsoft.com/be9332b5-8094-44a2-8632-af9957ecf36b">Constructing InParameters Objects and Parsing OutParameters Objects</a>.




## -remarks



If the method executed has input parameters, the <a href="https://msdn.microsoft.com/fba1bb97-29f9-41d3-8ecc-f283989118c1">InParameters</a> object in the <i>objWbemInParam</i> parameter must be the same as the description in 
the <a href="https://msdn.microsoft.com/be9332b5-8094-44a2-8632-af9957ecf36b">Constructing InParameters Objects and Parsing OutParameters Objects</a> topics.

Use <b>SWbemServices.ExecMethodAsync</b> as an alternative to direct access for executing a <a href="gloss_p.htm">provider method</a> when it is not possible to execute a method directly. For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters. Otherwise, it is recommended  that you use  direct access to invoke a method. For more information, see 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>.

The <b>SWbemServices.ExecMethodAsync</b> method requires an object path. If the script already contains an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object, you can call <a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">SWbemObject.ExecMethodAsync</a>.

This call returns immediately.  The status information is returned to the caller through call-backs delivered to the sink that is specified in <i>objWbemSink</i>. To continue processing when the call is completed, implement a subroutine for the   <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. For more information about how to eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.

Use the  <i>objWbemAsyncContext</i> parameter to verify the source of a call.


#### Examples

The following code example shows the 
<b>ExecMethodAsync</b> method. The script creates a 
<a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> object that represents a process that is running Notepad. It shows the setting up of an 
<a href="https://msdn.microsoft.com/fba1bb97-29f9-41d3-8ecc-f283989118c1">InParameters</a> object and how to obtain results from an 
<a href="https://msdn.microsoft.com/ae7774f7-8a53-44e4-a110-2aef9ae4037f">OutParameters</a> object. For a script that shows the same operations performed synchronously, see 
<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a>. For an example of using direct access, see 
<a href="https://msdn.microsoft.com/be80abec-fab4-4403-bc29-d0d4a38e3c87">Create Method in Class Win32_Process</a>. For an example of the same operation using <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, see 
<a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">SWbemObject.ExecMethodAsync</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &amp;VBCR &amp; "ReturnValue = " _
        &amp; oOutParams.ReturnValue &amp;VBCR &amp; _
        "ProcessId = " &amp; oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        &amp; hex(HResult)
    bdone = true
end sub</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9c692bc7-246b-4619-a371-cc9e0e2d5a6e">Calling a Provider Method</a>



<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>



<a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">SWbemObject.ExecMethodAsync_</a>



<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod_</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">SWbemServices.ExecMethod</a>
 

 

