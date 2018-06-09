---
UID: NN:wbemdisp.ISWbemObject
title: ISWbemObject
author: windows-sdk-content
description: You can use the methods and properties of the SWbemObject object to represent one Windows Management Instrumentation (WMI) class definition or object instance.
old-location: wmi\swbemobject.htm
old-project: WmiSdk
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemObject, SWbemObject, SWbemObject object [Windows Management Instrumentation], SWbemObject object [Windows Management Instrumentation],described, _hmm_swbemobject, wbemdisp/SWbemObject, wmi.swbemobject
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
 - SWbemObject
 - ISWbemObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject interface


## -description


You can use the methods and properties of the 
<b>SWbemObject</b> object to represent one  Windows Management Instrumentation (WMI) class definition or object instance. This object cannot be created by the VBScript <a href="https://msdn.microsoft.com/en-us/library/xzysf6hc(v=vs.84).aspx">CreateObject</a> call.

This object supports two types of properties and methods. Those defined in this section are generic properties and methods that apply to all WMI objects. In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of 
<b>SWbemObject</b>. The names and types of these properties and methods depend on the underlying WMI object. For more information about how these dynamic properties and methods are exposed, see 
<a href="https://msdn.microsoft.com/682cbe12-1487-4681-8d2f-4caf21cb068a">Manipulating Class and Instance Information</a>.

From the WMI client perspective, this object is always in-process. Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy. Updates to WMI are performed only when entire objects are written using a call to the 
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a> method. If you modify the properties or methods in an 
<b>SWbemObject</b>
    object, your changes are not written to WMI until you call 
<b>SWbemObject.Put_</b>.

The generic method and property names defined in this section always end with a trailing underscore ("_") to differentiate them from the dynamic WMI methods and properties of the underlying object.

Note that 
<b>SWbemObject</b> cannot be created using the VBScript 
<a href="47dd01cb-9468-481e-be7e-55f69a744635">GetObject</a>.method. If you want to create a new, empty class use 
<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a> with an empty path parameter. This call returns an empty 
<b>SWbemObject</b> object that can become a class. You can then supply a class name for the 
<a href="https://msdn.microsoft.com/60123963-31be-4112-9d06-611b4c599fd4">Class</a> property of the 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object returned by the 
<a href="https://msdn.microsoft.com/85a55159-5f10-49b5-bc37-39d7b4dfccd7">Path_</a> call. Add properties to the new class by the 
<a href="https://msdn.microsoft.com/8dd49678-47e7-4c6b-ab12-42532065eaf2">Properties_</a> method. To create an instance, call 
<b>GetObject</b> on the new class.

The following code example shows how to obtain a new class and add a property to it. The 
<b>SWbemObject</b> object that represents the class must be written back to the WMI repository by a call to 
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">Put_</a>.
<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

</pre>
</td>
</tr>
</table></span></div>
  You can examine the repository with a viewing tool such as <a href="further_information.htm">CIM Studio</a> to verify that the new class and instance appear. For an example of removing a class and instance from the repository, see <a href="https://msdn.microsoft.com/7dabab12-e8ee-4d44-932f-f3239b6f066e">SWbemServices.Delete</a> or <a href="https://msdn.microsoft.com/bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb">SWbemObject.Delete_</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObject</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>SWbemObject</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">Associators_</a>
</td>
<td align="left" width="63%">
Retrieves the associators of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c71e11cd-39a5-40d8-b279-f5ee9ff3ae04">AssociatorsAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously retrieves the associators of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">Clone_</a>
</td>
<td align="left" width="63%">
Makes a copy of the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38813551-2403-4def-ae57-2b17f72cd180">CompareTo_</a>
</td>
<td align="left" width="63%">
Tests two objects for equality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb">Delete_</a>
</td>
<td align="left" width="63%">
Deletes the object from WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8d67fa5-5217-422b-acbe-5eea6028deeb">DeleteAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously deletes the object from WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39a8a6e7-b499-410a-8c27-d4a05d1a61b9">ExecMethod_</a>
</td>
<td align="left" width="63%">
Executes a method exported by a method provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b848b38b-c0c3-49cd-b1e2-b0a440b82d61">ExecMethodAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously executes a method exported by a method provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b980863-14ad-4884-8897-dd076d927824">GetObjectText_</a>
</td>
<td align="left" width="63%">
Retrieves the textual representation of the object (MOF syntax).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30402d7d-f7cb-43b5-96b5-a8a76144e32d">Instances_</a>
</td>
<td align="left" width="63%">
Returns a collection of instances of the object (which must be a WMI class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d10fcbbf-6110-4152-8201-db43dc7a3c14">InstancesAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously returns a collection of instances of the object (which must be a WMI class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">Put_</a>
</td>
<td align="left" width="63%">
Creates or updates the object in WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff738412-fcca-4e4a-a178-0d1d391ec99b">PutAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously creates or updates the object in WMI.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba02da47-0bb2-40e1-af50-1c42b4be2abd">References_</a>
</td>
<td align="left" width="63%">
Returns references to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44989726-3f68-453b-b9f5-e76fb0fbb152">ReferencesAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously returns references to the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc">SpawnDerivedClass_</a>
</td>
<td align="left" width="63%">
Creates a new derived class from the current object (which must be a WMI class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4761bdb2-455a-48c4-9e22-bfba6a1036ec">SpawnInstance_</a>
</td>
<td align="left" width="63%">
Creates a new instance from the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c17e5d4a-016f-42ae-bc11-e21a44772ce5">Subclasses_</a>
</td>
<td align="left" width="63%">
Returns a collection of subclasses of the object (which must be a WMI class).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14d4a609-3aa4-49bd-bea4-6a71bc24d9dd">SubclassesAsync_</a>
</td>
<td align="left" width="63%">
Asynchronously returns a collection of subclasses of the object (which must be a WMI class).

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">SWbemObject</b> object has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a4daab0-7d10-4a37-aacd-1f3f499b859a">Derivation_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains an array of strings that describes the derivation hierarchy for the class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ef9abced-5126-4698-b01e-f3e9c871162f">Methods_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An 
<a href="https://msdn.microsoft.com/0ca2601f-ed40-472e-b4f2-eee750c8c8d1">SWbemMethodSet</a> object that is the collection of methods for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/85a55159-5f10-49b5-bc37-39d7b4dfccd7">Path_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object that represents the object path of the current class or instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8dd49678-47e7-4c6b-ab12-42532065eaf2">Properties_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An 
<a href="https://msdn.microsoft.com/0edad17b-facc-4885-9ce4-561ca6f57a66">SWbemPropertySet</a> object that is the collection of properties for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5ecae751-0d83-4ad6-9840-ef47f76b1ff6">Qualifiers_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An 
<a href="https://msdn.microsoft.com/7ac5469c-357b-499d-a558-30bf760c5311">SWbemQualifierSet</a> object that is the collection of qualifiers for this object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/add77267-d62f-4ee4-a0ff-8ca06a6bf7cd">Security_</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Contains an 
<a href="https://msdn.microsoft.com/794587fa-5feb-455b-be28-ecfaa25625ad">SWbemSecurity</a> object used to read or change the security settings.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/944d4cdc-ad35-4b53-b755-f10131a087fb">SWbemObjectEx</a>



<a href="https://msdn.microsoft.com/91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26">Scripting API Objects</a>
 

 

