---
UID: NF:wbemdisp.ISWbemObject.Delete_
title: ISWbemObject::Delete_
author: windows-sdk-content
description: The Delete_ method of the SWbemObject object deletes either the current class or the current instance.
old-location: wmi\swbemobject_delete_.htm
old-project: WmiSdk
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: Delete_, Delete_ method [Windows Management Instrumentation], Delete_ method [Windows Management Instrumentation],ISWbemObject interface, Delete_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],Delete_ method, ISWbemObject.Delete_, ISWbemObject::Delete_, SWbemObject object [Windows Management Instrumentation],Delete_ method, SWbemObject.Delete_, _hmm_swbemobject.delete_, wmi.swbemobject_delete_
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
 - SWbemObject.Delete_
 - ISWbemObject.Delete_
 - ISWbemObject.Delete_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::Delete_


## -description


The 
<b>Delete_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object deletes either the current class or the current instance. If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion. For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Reserved and must be 0 (zero) if specified.


### -param objWbemNamedValueSet






#### - objwbemNamedValueSet [in, optional]

This parameter is typically undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



This method does not return a value.




## -remarks



The 
<b>Delete_</b> method  fails if a new instance of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> is created, but no value is supplied for the key property. Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by <b>SWbemObject.Delete_</b>. In this case, 
<a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">SWbemServices.Delete</a>, which uses the object path works. Note that an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object is returned by the 
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a> method after an object is committed to WMI.


#### Examples

The following example creates a new class;  adds a key property; writes the new class to the repository; and displays the path of the new class object. The script then spawns an instance of the new class; writes it; and displays the path. Note that the script deletes both the class and its instances from the repository by simply deleting the class.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
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


