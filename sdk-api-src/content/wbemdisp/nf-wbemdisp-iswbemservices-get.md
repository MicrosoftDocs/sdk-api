---
UID: NF:wbemdisp.ISWbemServices.Get
title: ISWbemServices::Get
author: windows-sdk-content
description: Retrieves an object, that is either a class definition or an instance, based on the object path.
old-location: wmi\swbemservices_get.htm
old-project: WmiSdk
ms.assetid: 3071aeb2-adab-47aa-a10c-9796766bb630
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Get, Get method [Windows Management Instrumentation], Get method [Windows Management Instrumentation],ISWbemServices interface, Get method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],Get method, ISWbemServices.Get, ISWbemServices::Get, SWbemServices object [Windows Management Instrumentation],Get method, SWbemServices.Get, _hmm_swbemservices.get, wbemFlagUseAmendedQualifiers, wmi.swbemservices_get
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
 - SWbemServices.Get
 - ISWbemServices.Get
 - ISWbemServices.Get
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::Get


## -description


The <b>Get</b> method of the 
    <a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object retrieves an object, that is 
    either a class definition or an instance, based on the object path. This method retrieves only objects 
    from the namespace that is associated with the current 
    <b>SWbemServices</b> object.

The method is called in the synchronous mode. For more information, see 
    <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
    <a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strObjectPath [optional]

String that contains the object path of the object to retrieve. If this value is empty, the empty object 
      that is returned can become a new class. For more information, see 
      <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param iFlags [optional]

Integer that determines the behavior of the query. This parameter can accept the following values.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. For more information about 
        amended qualifiers, see 
        <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
      <a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent 
      the context information that can be used by the provider that is servicing the request. A provider that supports 
      or requires such information must document the recognized value names, data type of the value, allowed values, 
      and semantics.


### -param objWbemObject






## -returns



If successful, this method returns an 
       <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that represents the requested object.




## -remarks



Unlike the <a href="https://msdn.microsoft.com/94d5c8ee-2d61-42af-9a22-cc0df423b245">ExecQuery</a> and 
    <a href="https://msdn.microsoft.com/6465a981-f98e-4ece-a9b6-9da8ae618bc6">InstancesOf</a> methods, the Get method always 
    returns an <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> representing a specific instance of a 
    WMI-managed resource. To obtain a specific instance of a WMI-managed resource using the Get method, you must tell 
    Get the instance to retrieve by passing the method the object path, as shown in the following script.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" &amp; strComputer &amp; "\root\cimv2")
Set objSWbemObject = objSWbemServices.Get("Win32_Service.Name='Messenger'")
Wscript.Echo "Name:         " &amp; objSWbemObject.Name        &amp; vbCrLf &amp; _
             "Display Name: " &amp; objSWbemObject.DisplayName &amp; vbCrLf &amp; _
             "Start Mode:   " &amp; objSWbemObject.StartMode   &amp; vbCrLf &amp; _
             "State:        " &amp; objSWbemObject.State
</pre>
</td>
</tr>
</table></span></div>
You can  use this method to obtain <a href="gloss_s.htm">singleton</a> objects, such as <a href="https://msdn.microsoft.com/907b65b2-a853-40f4-8b36-5a05a2b1cf85">__CIMOMIdentification</a>, which contains version information about the WMI installation that is running.

You can examine the repository with a viewing tool such as <a href="further_information.htm">CIM Studio</a> to verify that the new class and instance appear. For an example of removing a class and instance from the repository, see <a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">SWbemServices.Delete</a> or <a href="https://msdn.microsoft.com/bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb">SWbemObject.Delete_</a>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

