---
UID: NF:wbemdisp.ISWbemObject.ExecMethodAsync_
title: ISWbemObject::ExecMethodAsync_
author: windows-sdk-content
description: The ExecMethodAsync_ method of SWbemObject asynchronously executes a method that a method provider exports.
old-location: wmi\swbemobject_execmethodasync_.htm
old-project: WmiSdk
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ExecMethodAsync_, ExecMethodAsync_ method [Windows Management Instrumentation], ExecMethodAsync_ method [Windows Management Instrumentation],ISWbemObject interface, ExecMethodAsync_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],ExecMethodAsync_ method, ISWbemObject.ExecMethodAsync_, ISWbemObject::ExecMethodAsync_, SWbemObject object [Windows Management Instrumentation],ExecMethodAsync_ method, SWbemObject.ExecMethodAsync_, _hmm_swbemobject.execmethodasync_, wbemFlagDontSendStatus, wbemFlagSendStatus, wmi.swbemobject_execmethodasync_
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
 - SWbemObject.ExecMethodAsync_
 - ISWbemObject.ExecMethodAsync_
 - ISWbemObject.ExecMethodAsync_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::ExecMethodAsync_


## -description


The 
<b>ExecMethodAsync_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>  asynchronously executes a method that a method provider exports. This method is similar to 
<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">SWbemServices.ExecMethodAsync</a>, but operates directly on the object of the method to be executed. Windows Management Instrumentation (WMI) does not implement this method. The provider implements this method.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink [in]

Required. This is the object sink that receives the results of the method call. The outbound parameters are sent to the 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">SWbemSink.OnObjectReady</a> event of the supplied object sink. The results of the call mechanism are sent to the 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">SWbemSink.OnCompleted</a> event of the supplied object sink. Notice that <b>SWbemSink.OnCompleted</b> does not receive the return code of the method. However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons. The result code returned from the method is returned in the outbound parameter object supplied to <b>SWbemSink.OnObjectReady</b>. If any error code returns, then the supplied 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a> object is not used. If the call is successful, then the user's <b>IWbemObjectSink</b> implementation is called to indicate the result of the operation.


### -param strMethodName [in]

Required. This is the name of the method for the object.


### -param objWbemInParameters




### -param iFlags [in, optional]

Integer that determines the behavior of the call. This parameter can accept the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">SWbemSink.OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.


### -param objWbemNamedValueSet




### -param objWbemAsyncContext [in, optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter if you are making multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. This <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - objwbemInParams [in, optional]

This is an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains the input parameters for the method being executed. By default, this parameter is undefined. For more  information, see 
<a href="https://msdn.microsoft.com/8cc65129-1698-4ada-b493-672772c94045">Constructing InParameters Objects</a> and <a href="https://msdn.microsoft.com/fc06d6a1-770a-4f34-affd-f5035dad9360">Parsing OutParameters Objects</a>.


#### - objwbemNamedValueSet [in, optional]

Typically, it is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method has no return values. If the call is successful, an 
<a href="https://msdn.microsoft.com/ae7774f7-8a53-44e4-a110-2aef9ae4037f">OutParameters</a> object, which is also an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object, is supplied to the sink specified in <i>objWbemSink</i>. The returned <b>OutParameters</b> object contains the output parameters and return value for the method being executed.




## -remarks



Use the <b>SWbemObject.ExecMethodAsync_</b> method as an alternative to direct access for executing a <a href="https://msdn.microsoft.com/en-us/library/Aa390825(v=VS.85).aspx">provider method</a> when you cannot execute  a method directly. For example, if your method has out parameters, use the <b>SWbemObject.ExecMethodAsync_</b> method with a scripting language that does not support output parameters. Otherwise, it is recommended that you invoke a method using direct access. For more information, see 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>.

This call returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it arrives, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned, you can perform final processing in your implementation of the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, use either semisynchronous communication or synchronous communication.
For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

If the method being executed has input parameters, the <a href="https://msdn.microsoft.com/fba1bb97-29f9-41d3-8ecc-f283989118c1">InParameters</a> object and <i>objWbemInParam</i> parameter must be constructed as described in 
<a href="https://msdn.microsoft.com/8cc65129-1698-4ada-b493-672772c94045">Constructing InParameters Objects</a> and <a href="https://msdn.microsoft.com/fc06d6a1-770a-4f34-affd-f5035dad9360">Parsing OutParameters Objects</a>.

The <b>SWbemObject.ExecMethodAsync_</b> method assumes the object represented by <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> contains the method to execute. The <a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">SWbemServices.ExecMethodAsync</a> method requires an object path.


#### Examples

The following example shows the 
<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">ExecMethodAsync</a> method. The script creates a 
<a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a> object that represents a process that is running Notepad. It shows setting up of 
<a href="https://msdn.microsoft.com/fba1bb97-29f9-41d3-8ecc-f283989118c1">InParameters</a> object, and how to obtain results from an 
<a href="https://msdn.microsoft.com/ae7774f7-8a53-44e4-a110-2aef9ae4037f">OutParameters</a> object.

For a script that shows the same operations performed synchronously, see 
<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">SWbemObject.ExecMethod</a>. For an example using direct access, see 
 <a href="https://msdn.microsoft.com/be80abec-fab4-4403-bc29-d0d4a38e3c87">Create Method in Class Win32_Process</a>. For an example of the same operation using an <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object, see 
<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">SWbemServices.ExecMethodAsync</a>.


```vb
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
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

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```





## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">SWbemServices.ExecMethodAsync</a>
 

 

