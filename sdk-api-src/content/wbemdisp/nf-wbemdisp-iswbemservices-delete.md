---
UID: NF:wbemdisp.ISWbemServices.Delete
title: ISWbemServices::Delete
author: windows-sdk-content
description: Deletes the class or instance that is specified in the object path. You can only delete objects in the current namespace.
old-location: wmi\swbemservices_delete.htm
old-project: WmiSdk
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: Delete, Delete method [Windows Management Instrumentation], Delete method [Windows Management Instrumentation],ISWbemServices interface, Delete method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],Delete method, ISWbemServices.Delete, ISWbemServices::Delete, SWbemServices object [Windows Management Instrumentation],Delete method, SWbemServices.Delete, _hmm_swbemservices.delete, wmi.swbemservices_delete
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
 - SWbemServices.Delete
 - ISWbemServices.Delete
 - ISWbemServices.Delete
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::Delete


## -description


The 
<b>Delete</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object deletes the class or instance that is specified in the object path. You can only delete objects in the current namespace.

If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.

This method is called in the synchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strObjectPath

Required. String that contains the object path to the object  that you want to delete. For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param iFlags [optional]

Reserved. This value must be zero.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that  services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value.




## -remarks



The <b>SWbemServices.Delete</b> method can be used when the key property for the object is not  given a value, because this method only requires an object path as input. This method can be used in situations where <a href="https://msdn.microsoft.com/bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb">SWbemObject.Delete_</a>  fails for lack of a key value. If the object is committed to WMI through <a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a>, then an <a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object was obtained through the call.


#### Examples

The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object. The script then spawns an instance of the new class, writes the instance, and displays the path. Note that the script deletes both the class and its instances from the repository by  deleting the class. For more information about WMI classes and instances, see <a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a> and <a href="https://msdn.microsoft.com/3e619cb7-18a9-40ff-82fe-c10eb5090a93">Common Information Model</a>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err &lt;&gt; 0 Then
    WScript.Echo Err.Number &amp; "    " &amp; Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

