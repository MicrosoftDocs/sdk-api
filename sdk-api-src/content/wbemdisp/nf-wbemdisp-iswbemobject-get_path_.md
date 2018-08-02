---
UID: NF:wbemdisp.ISWbemObject.get_Path_
title: ISWbemObject::get_Path_
author: windows-sdk-content
description: The Path_ property of the SWbemObject object returns an SWbemObjectPath object that represents the object path of the current class or instance. This property can be passed as a parameter to methods that require an object path.
old-location: wmi\swbemobject_path_.htm
old-project: WmiSdk
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],Path_ property, ISWbemObject.get_Path_, ISWbemObject::get_Path_, Path_ property [Windows Management Instrumentation], Path_ property [Windows Management Instrumentation],ISWbemObject interface, Path_ property [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],Path_ property, SWbemObject.Path_, _hmm_swbemobject.path_, get_Path_, wmi.swbemobject_path_
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
 - SWbemObject.Path_
 - ISWbemObject.Path_
 - ISWbemObject.get_Path_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::get_Path_


## -description


The 
<b>Path_</b> property of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object that represents the object path of the current class or instance. This property can be passed as a parameter to methods that require an object path.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.

This property is read-only.


## -parameters


## -remarks



Only the 
<a href="https://msdn.microsoft.com/60123963-31be-4112-9d06-611b4c599fd4">Class</a> property of the returned 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> instance can be modified. If you try to modify any other property, or try to call the methods 
<a href="https://msdn.microsoft.com/d341b980-bac9-4db4-a55f-eb971fb385da">SetAsClass</a> or 
<a href="https://msdn.microsoft.com/7ec53954-2aac-494c-87c7-6a14592d8bd5">SetAsSingleton</a>, you will get a <b>wbemErrReadOnly</b> error.

Because of this, you cannot modify the 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object that is the value of the 
<a href="https://msdn.microsoft.com/1919403d-6dea-4d41-9bc7-a622a9c9c2c8">Keys</a> property of the returned 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> instance. If you try to call the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>, 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>, or 
<a href="https://msdn.microsoft.com/db5d2e68-028e-4902-ad42-0b46e1a96bcb">DeleteAll</a> methods on this value, you will get a wbemErrReadOnly error. Furthermore, you cannot modify any 
<a href="https://msdn.microsoft.com/3f72afcd-6e10-4200-804d-918e3eb2862f">SWbemNamedValue</a> obtained from this collection. Attempts to modify the 
<b>Value</b> property return the same error code.

However, if you call 
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a> to create a copy, the 
<a href="https://msdn.microsoft.com/cc0d2c56-bb69-4008-8688-0166714ea5fd">SWbemObjectPath.Path</a>property of the copy is fully modifiable.


#### Examples

The following code sample, taken from <a href="https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517">List All the WMI cimV2 Classes</a> in the TechNet Gallery, uses the Path_ property to list all the WMI cimV2 classes.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" &amp; _  
    strComputer &amp; "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next </pre>
</td>
</tr>
</table></span></div>


