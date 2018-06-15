---
UID: NN:wbemdisp.ISWbemServices
title: ISWbemServices
author: windows-sdk-content
description: You can use the methods of an SWbemServices object to perform operations against a namespace on either a local host or a remote host. This object cannot be created by the VBScript CreateObject call.
old-location: wmi\swbemservices.htm
old-project: WmiSdk
ms.assetid: 7fcfa404-2fe6-42e5-85ac-64536f6d2a44
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServices, SWbemServices, SWbemServices object [Windows Management Instrumentation], SWbemServices object [Windows Management Instrumentation],described, _hmm_swbemservices, wbemdisp/SWbemServices, wmi.swbemservices
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - SWbemServices
 - ISWbemServices
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices interface


## -description


You can use the methods of an 
<b>SWbemServices</b> object to perform operations against a namespace on either a local host or a remote host. This object cannot be created by the VBScript <b>CreateObject</b> call.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemServices</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemServices</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">AssociatorsOf</a>
</td>
<td align="left" width="63%">
Retrieves the instances of managed resources that are associated with a specified resource through one or more association classes. You provide the object path for the originating endpoint, and <a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">AssociatorsOf</a> returns the managed resources at the opposite endpoint. The <b>AssociatorsOf</b> method performs the same function that the "ASSOCIATORS OF" WQL query performs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3969d90f-d39c-40f1-9328-fc1afbaa53b1">AssociatorsOfAsync</a>
</td>
<td align="left" width="63%">
Asynchronously returns a collection of objects (classes or instances) that are associated with a specified object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">Delete</a>
</td>
<td align="left" width="63%">
Deletes an instance of a managed resource (or a class definition from the CIM repository).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f5ed170e-d002-4dd9-b8b6-b764a7a41a27">DeleteAsync</a>
</td>
<td align="left" width="63%">
Asynchronously deletes the class or instance that is specified in the object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">ExecMethod</a>
</td>
<td align="left" width="63%">
Provides an alternative way to execute a method defined by a managed resource class definition. Primarily used in situations in which the scripting language does not support out parameters. For example, JScript does not support out parameters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/933a4c64-7538-474e-9f6f-f94da6066b46">ExecMethodAsync</a>
</td>
<td align="left" width="63%">
Asynchronously executes a method that is exported by a method provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e1bb428-5395-4e90-9713-6d96242fef4e">ExecNotificationQuery</a>
</td>
<td align="left" width="63%">
Executes an event subscription query to receive events. An event subscription query is a query that defines a change to the managed environment that you want to monitor. When the change occurs, the WMI infrastructure delivers an event describing the change to the calling script.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b0e8313-4ffd-4d4a-8965-d2c6743e7573">ExecNotificationQueryAsync</a>
</td>
<td align="left" width="63%">
Asynchronously executes a query to receive events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">ExecQuery</a>
</td>
<td align="left" width="63%">
Executes a query to retrieve a collection of instances of WMI-managed resources (or class definitions). <a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">ExecQuery</a> can be used to retrieve a filtered collection of instances that match criteria you define in the query passed to <b>ExecQuery</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50c7f62b-dd83-4117-b10e-acee1690ce8c">ExecQueryAsync</a>
</td>
<td align="left" width="63%">
Asynchronously executes a query to retrieve objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Retrieves a single instance of a managed resource (or class definition) based on an object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8da46851-52b8-4b5a-8c9d-1d492f57f4b6">GetAsync</a>
</td>
<td align="left" width="63%">
Asynchronously retrieves an object, that is either a class definition or an instance, based on the object path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a>
</td>
<td align="left" width="63%">
Retrieves all the instances of a managed resource based on a class name. By default, <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a> performs a deep retrieval. That is, <b>InstancesOf</b> retrieves the instances of the resource identified by the class name passed to the method and also retrieves all the instances of all the resources that are subclasses (defined beneath) of the target class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/631cd749-9a39-4606-9a38-0b4bb5b4b2cd">InstancesOfAsync</a>
</td>
<td align="left" width="63%">
Asynchronously returns the instances of a specified class according to the user-specified selection criteria.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">ReferencesTo</a>
</td>
<td align="left" width="63%">
Returns all of the associations that reference a specified resource. The best way to understand <a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">ReferencesTo</a> is to compare it with the <a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">AssociatorsOf</a> method. <b>AssociatorsOf</b> returns the dynamic resources that are at the opposite end of an association. <b>ReferencesTo</b> returns the association itself. The <b>ReferencesTo</b> method performs the same function that the "REFERENCES OF" WQL query performs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">ReferencesToAsync</a>
</td>
<td align="left" width="63%">
Asynchronously returns a collection of all association classes or instances that refer to a specific class or instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cfe08956-7215-4e2e-a279-6e86f14e5c27">SubclassesOf</a>
</td>
<td align="left" width="63%">
Retrieves all the subclasses of a specified class from the CIM repository.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9d16ee9-992e-4ce5-9c03-0a2c9958588c">SubclassesOfAsync</a>
</td>
<td align="left" width="63%">
Asynchronously returns a collection of subclasses for a specified class.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemServices</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d8b1118b-b26d-4740-915e-484a83953b11">Security_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Used to get or set the security settings for an <b>SWbemServices</b> object.

</td>
</tr>
</table> 


## -remarks



The methods can be called in either the synchronous mode, the asynchronous mode, or the semisynchronous mode. For more information see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

<b>Overview</b>

<b>SWbemServices</b> serves two primary roles. First, the <b>SWbemServices</b> object represents an authenticated connection to a WMI namespace on a target computer. Second, <b>SWbemServices</b> is the Automation object you use to retrieve WMI-managed resources. You can obtain a reference to an <b>SWbemServices</b> object in either of two ways:

<ul>
<li>
As demonstrated in most of the WMI scripts presented thus far, you can use the VBScript <a href="https://msdn.microsoft.com/library/windows/desktop/47dd01cb-9468-481e-be7e-55f69a744635">GetObject</a> function in combination with the WMI moniker "winmgmts:". The following example is the simplest form of a WMI connection. The example connects to the default namespace (typically "Root\CIMv2") on the local computer:

<code>Set objSWbemServices = GetObject("winmgmts:")
</code>

</li>
<li>You can also use the <a href="https://msdn.microsoft.com/51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee">SWbemLocator</a> object <a href="https://msdn.microsoft.com/92222e08-8622-46c3-9465-cd12260a2ca0">ConnectServer</a> method to obtain a reference to an <b>SWbemServices</b> object.</li>
</ul>
After you obtain a reference to an <b>SWbemServices</b> object, you use the object reference to call 1 of 18 methods available using <b>SWbemServices</b>. <b>SWbemServices</b> can return one of three different WMI scripting library objects (<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>, <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>, or <a href="https://msdn.microsoft.com/7efd5e6a-4311-4d20-8b05-e9208eec098a">SWbemEventSource</a>), depending on the method you call. Knowing the type of object each method returns will help you determine the next step your script must take. For example, if you get back an <b>SWbemObjectSet</b>, you must enumerate the collection to access each <b>SWbemObject</b> in the collection. If you get back an <b>SWbemObject</b>, you can immediately access the object methods and properties without enumerating the collection first.

<b>Modes of Operation</b>

<b>SWbemServices</b> supports three modes of operation: synchronous, asynchronous, and semisynchronous.

<ul>
<li><b>Synchronous</b>. In synchronous mode, your script blocks (pauses) until the <b>SWbemServices</b> method completes. Not only does your script wait, but in cases in which WMI retrieves instances of managed resources, WMI builds the entire <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> in memory before the first byte of data is returned to the calling script. This can have an adverse effect on the script performance and on the computer running the script. For example, synchronously retrieving thousands of events from the Windows Event Logs can take a long time and use a lot of memory. For these reasons, synchronous operations are not recommended except for the three methods (<a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">Delete</a>, <a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">ExecMethod</a>, and <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>) that are synchronous by default. These methods do not return large data sets, so semisynchronous operation is not required.</li>
<li><b>Asynchronous</b>. In asynchronous mode, your script calls one of the nine asynchronous methods and returns immediately. That is, as soon as the asynchronous method is called, your script resumes running the next line of code. To use an asynchronous method, your script must first create an <a href="https://msdn.microsoft.com/a90777ef-fa26-4bfb-b196-c083a0c92a29">SWbemSink</a> object and a special subroutine called an event handler. WMI performs the asynchronous operation and notifies the script by calling the event handler subroutine when the operation is complete.</li>
<li>
<b>Semisynchronous</b>. Semisynchronous mode is a compromise between synchronous and asynchronous. Semisynchronous operations offer better performance than synchronous operations, yet they do not require the extra knowledge and scripting steps necessary to handle asynchronous operations. This is the default operation type for most WMI queries.

In semisynchronous mode, your script calls one of the six data retrieval methods and returns immediately. WMI retrieves the managed resources in the background as your script continues to run. As the resources are retrieved, they are immediately returned to your script by way of an SWbemObjectSet. You can begin to access the managed resources without waiting for the entire collection to be assembled.

There is a caveat to semisynchronous operations when you are working with managed resources that have many instances (many meaning greater than 1,000), such as <a href="https://msdn.microsoft.com/e90e1216-e943-4f3a-9f6c-8a0b4568a11f">CIM_DataFile</a> and <a href="https://msdn.microsoft.com/d2c96eef-3680-42f8-bdf1-f987a3e94257">Win32_NTLogEvent</a>. The caveat is a result of how WMI handles instances of managed resources. For each instance of a managed resource, WMI creates and caches an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object. When a large number of instances exist for a managed resource, instance retrieval can monopolize available resources, reducing the performance of both the script and the computer.

To work around the problem, you can optimize semisynchronous method calls using the <b>wbemFlagForwardOnly</b> flag. The <b>wbemFlagForwardOnly</b> flag, combined with the <b>wbemFlagReturnImmediately</b> flag (the default semisynchronous flag), tells WMI to return a forward-only <a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>, which eliminates the large data set performance problem. However, using the <b>wbemFlagForwardOnly</b> flag comes with a cost. A forward-only <b>SWbemObjectSet</b> can be enumerated only once. After each <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> in a forward-only <b>SWbemObjectSet</b> is accessed, the memory allocated to the instance is released.

</li>
</ul>
With the exception of the <a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">Delete</a>, <a href="https://msdn.microsoft.com/2637efdc-fde5-4a44-a41f-67e0fb0df19d">ExecMethod</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>, and nine asynchronous methods, semisynchronous is the default and recommended mode of operation.

<b>Commonly-used Methods</b>

The methods most often used in system administration scripts are <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a>, <a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">ExecQuery</a>, <a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>, and <a href="https://msdn.microsoft.com/3e1bb428-5395-4e90-9713-6d96242fef4e">ExecNotificationQuery</a>. Although often used, <b>InstancesOf</b> is not necessarily the recommended way to retrieve information (although it is arguably the easiest way).




## -see-also




<a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

