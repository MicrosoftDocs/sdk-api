---
UID: NF:wbemdisp.ISWbemServices.InstancesOf
title: ISWbemServices::InstancesOf
author: windows-sdk-content
description: Creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria.
old-location: wmi\swbemservices_instancesof.htm
old-project: WmiSdk
ms.assetid: 6465a981-f98e-4ece-a9b6-9da8ae618bc6
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServices interface [Windows Management Instrumentation],InstancesOf method, ISWbemServices.InstancesOf, ISWbemServices::InstancesOf, InstancesOf, InstancesOf method [Windows Management Instrumentation], InstancesOf method [Windows Management Instrumentation],ISWbemServices interface, InstancesOf method [Windows Management Instrumentation],SWbemServices object, SWbemServices object [Windows Management Instrumentation],InstancesOf method, SWbemServices.InstancesOf, _hmm_swbemservices.instancesof, wbemFlagBidirectional, wbemFlagForwardOnly, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemservices_instancesof
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
 - SWbemServices.InstancesOf
 - ISWbemServices.InstancesOf
 - ISWbemServices.InstancesOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::InstancesOf


## -description


The 
<b>InstancesOf</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object creates an enumerator that returns the instances of a specified class according to the user-specified selection criteria. This method implements a simple query. More complex queries may require the use of 
<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>.

The method is called in the semisynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strClass

Required. String that contains the name of the class for which instances are desired. This parameter cannot be blank.


### -param iFlags [optional]

This parameter determines how detailed the call enumerates and if this call returns immediately. The default value for this parameter is <b>wbemFlagReturnImmediately</b>. This parameter can accept the following values.



#### wbemFlagForwardOnly (32 (0x20))

Causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to 
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a>.



#### wbemFlagBidirectional (0 (0x0))

Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.



#### wbemFlagReturnImmediately (16 (0x10))

Default value for this parameter. This flag causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed. This flag calls the method in the synchronous mode.



#### wbemQueryFlagShallow (1 (0x1))

Forces the enumeration to include only immediate subclasses of the specified parent class.



#### wbemQueryFlagDeep (0 (0x0))

Default value for this parameter. This value forces the enumeration to include all classes in the hierarchy.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. 

       For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemObjectSet






## -returns



If successful, the method returns an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>.




## -remarks



The 
<b>InstancesOf</b> method only works for class objects.

By default, InstancesOf performs a deep retrieval. That is, InstancesOf retrieves all instances of the managed resource you identify and all instances of all the subclasses defined beneath the target class. For example, the following script retrieves all of the resources modeled by all of the dynamic classes defined beneath the CIM_Service abstract class.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" &amp; strComputer &amp; "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("CIM_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Object Path: " &amp; objSWbemObject.Path_.Path
Next</pre>
</td>
</tr>
</table></span></div>
If you run this script, you will get information back. However, this information will not be limited to the services installed on a computer. Instead, it will include information from all child classes of <a href="https://msdn.microsoft.com/b95e8ea7-4daf-4dcf-817c-b872560b62df">CIM_Service</a>, including <a href="https://msdn.microsoft.com/67dc6e14-c8c1-4168-8f99-b04c6ecd4ad2">Win32_SystemDriver</a> and <a href="https://msdn.microsoft.com/f1e947c7-bc88-4fe6-ae51-d4acc7317d79">Win32_ApplicationService</a>.




## -see-also




<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

