---
UID: NF:wbemdisp.ISWbemServices.ExecNotificationQueryAsync
title: ISWbemServices::ExecNotificationQueryAsync
author: windows-sdk-content
description: Executes a query to receive events.
old-location: wmi\swbemservices_execnotificationqueryasync.htm
old-project: WmiSdk
ms.assetid: 0b0e8313-4ffd-4d4a-8965-d2c6743e7573
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ExecNotificationQueryAsync, ExecNotificationQueryAsync method [Windows Management Instrumentation], ExecNotificationQueryAsync method [Windows Management Instrumentation],ISWbemServices interface, ExecNotificationQueryAsync method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],ExecNotificationQueryAsync method, ISWbemServices.ExecNotificationQueryAsync, ISWbemServices::ExecNotificationQueryAsync, SWbemServices object [Windows Management Instrumentation],ExecNotificationQueryAsync method, SWbemServices.ExecNotificationQueryAsync, _hmm_swbemservices.execnotificationqueryasync, wbemFlagDontSendStatus, wbemFlagSendStatus, wmi.swbemservices_execnotificationqueryasync
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
 - SWbemServices.ExecNotificationQueryAsync
 - ISWbemServices.ExecNotificationQueryAsync
 - ISWbemServices.ExecNotificationQueryAsync
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::ExecNotificationQueryAsync


## -description


The 
<b>ExecNotificationQueryAsync</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object executes a query  to receive events. This call returns immediately and the results and status are returned to the caller through events delivered to the sink that is specified in <i>objWbemSink</i>.

The events that are specified in the query can   be intrinsic  Windows Management Instrumentation (WMI) events, such as <a href="https://msdn.microsoft.com/41976479-70e3-4914-a56a-fa94a1fd31c7">__InstanceCreationEvent</a>, or extrinsic events, such as <a href="https://msdn.microsoft.com/a700467b-4535-4197-8aed-bae7e84e7962">Win32_IP4RouteTableEvent</a> or <a href="https://msdn.microsoft.com/2de566a8-6195-4325-b1d3-4ef37031cbda">RegistryKeyChangeEvent</a>. For more information, see <a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>.

The method is called in the asynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemSink

Required. Object sink that receives the notification of events asynchronously. Create a <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object to receive the objects.


### -param strQuery

Required. String that contains the text of the event-related query. This parameter cannot be blank. For more information on building WMI query strings, see <a href="https://msdn.microsoft.com/7e04ba37-c0e0-4304-b162-8b911f233f38">Querying with WQL</a> and the <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a> reference.


### -param strQueryLanguage [optional]

String that contains the query language to be used. If specified, this value must be "WQL".


### -param iFlags [optional]

Integer that determines the behavior of the query. This parameter can be set to the following values.



#### wbemFlagSendStatus (128 (0x80))

Causes asynchronous calls to send status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.



#### wbemFlagDontSendStatus (0 (0x0))

Prevents asynchronous calls from sending status updates to the 
<a href="https://msdn.microsoft.com/abb43916-f952-41fe-a5ba-0428864c0685">OnProgress</a> event handler for the object sink.


### -param objWbemNamedValueSet




### -param objWbemAsyncContext [optional]

This is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that returns to the object sink to identify the source of the original asynchronous call. Use this parameter to make multiple asynchronous calls using the same object sink. To use this parameter, create an <b>SWbemNamedValueSet</b> object and use the <a href="https://msdn.microsoft.com/471b23f5-6c53-40e2-a2a9-0798044c9dfb">SWbemNamedValueSet.Add</a> method to add a value that identifies the asynchronous call you are making. The <b>SWbemNamedValueSet</b> object is returned to the object sink and the source of the call can be extracted using the <a href="https://msdn.microsoft.com/ccebe65e-6032-43d5-9004-2247c3b96d6d">SWbemNamedValueSet.Item</a> method. For more information, see 
<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.


#### - objwbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value. If successful, the sink receives an 
<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event per instance. After the last instance, the object sink receives an 
<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.




## -remarks



The <b>ExecNotificationQueryAsync</b> method returns event type objects that future events generate. The event objects that 
<b>ExecNotificationQueryAsync</b> requests can be intrinsic (for example, <a href="https://msdn.microsoft.com/41976479-70e3-4914-a56a-fa94a1fd31c7">__InstanceCreationEvent</a>), or extrinsic (for example, <a href="https://msdn.microsoft.com/2de566a8-6195-4325-b1d3-4ef37031cbda">RegistryKeyChangeEvent</a> or SNMP events). For more information, see 
<a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>.

The call to <b>ExecNotificationQueryAsync</b> returns immediately.  The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in <i>objWbemSink</i>. To process each object when it is returned, create an <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/14110ee7-a808-4786-b695-2ce54189d826">OnObjectReady</a> event subroutine. After all the objects are returned,  perform the final processing to implement the  <i>objWbemSink</i>.<a href="https://msdn.microsoft.com/2723185d-5b8b-4cc7-ada3-51c3275272a9">OnCompleted</a> event.

An asynchronous callback allows a non-authenticated user to provide data to the sink. This poses security risks to your scripts and applications. To eliminate the risks, see <a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>.

There are limits to the number of <b>AND</b> and <b>OR</b> keywords that can be used in WQL queries.  Large numbers of WQL keywords used in a complex query can cause WMI to return the <b>WBEM_E_QUOTA_VIOLATION</b> error code asan <b>HRESULT</b> value.  The limit of WQL keywords depends on how complex the query is.


#### Examples

The following VBScript code example shows a script  that is waiting for a WMI  event notification that indicates that a process has terminated. It is waiting for a WMI intrinsic event, an instance of the event class <a href="https://msdn.microsoft.com/a370fc95-15e3-49c3-98de-2f40d742f207">__InstanceDeletionEvent</a>. The <b>__InstanceDeletionEvent</b> must represent the deletion of an instance of <a href="https://msdn.microsoft.com/51206aca-4784-4d18-95ca-bc0a45691f78">Win32_Process</a>. For more information about WMI intrinsic events, see <a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>.

The following script runs indefinitely until the computer is rebooted, WMI is stopped, or the script is stopped. To stop the script manually, use Task Manager to stop the process. To stop it programmatically, use the <a href="https://msdn.microsoft.com/6c6b27d4-cf9b-42d7-9136-42641ea56ee8">Terminate</a>  method in the Win32_Process class.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" &amp; _strComputer &amp; "\root\CIMV2") 
Set MySink = WScript.CreateObject("WbemScripting.SWbemSink","SINK_")

objWMIservice.ExecNotificationQueryAsync MySink, "SELECT * FROM __InstanceCreationEvent WITHIN 1 " _
                                               &amp; "WHERE TargetInstance ISA 'Win32_Process'"

WScript.Echo "Waiting for events..."

While (True)
    Wscript.Sleep(1000)
Wend

Sub SINK_OnObjectReady(objObject, objAsyncContext)
    WScript.Echo "Event occurred."
End Sub

Sub SINK_OnCompleted(objObject, objAsyncContext)
    WScript.Echo "Event call complete."
End Sub</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/46cdfcfa-42c6-4169-bc4d-725867224889">Determining the Type of Event to Receive</a>



<a href="https://msdn.microsoft.com/4cac5fdd-c842-4d7e-a56e-2e1312df68b4">Registering for System Registry Events</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>



<a href="https://msdn.microsoft.com/50c7f62b-dd83-4117-b10e-acee1690ce8c">SWbemServices.ExecQueryAsync</a>



<a href="https://msdn.microsoft.com/2b839ea9-e1e6-4123-a98a-04ebee907b3b">Setting Security on an Asynchronous Call</a>
 

 

