---
UID: NN:wbemcli.IWbemClassObject
title: IWbemClassObject
author: windows-sdk-content
description: Contains and manipulates both class definitions and class object instances.
old-location: wmi\iwbemclassobject.htm
old-project: WmiSdk
ms.assetid: a3ce37d7-5580-4b84-9119-78412c8e0d27
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: IWbemClassObject, IWbemClassObject interface [Windows Management Instrumentation], IWbemClassObject interface [Windows Management Instrumentation],described, WbemClassObject, _hmm_iwbemclassobject, wbemcli/IWbemClassObject, wmi.iwbemclassobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CIMWin32.dll
-	Esscli.dll
-	Fastprox.dll
-	FrameDyn.dll
-	FrameDynOS.dll
-	Krnlprov.dll
-	Ncprov.dll
-	Wbemcore.dll
-	Wbemess.dll
-	Wmipiprt.dll
api_name:
-	IWbemClassObject
-	WbemClassObject
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject interface


## -description


The <b>IWbemClassObject</b> interface 
    contains and manipulates both class definitions and class object instances.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemClassObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemClassObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemClassObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">BeginEnumeration</a>
</td>
<td align="left" width="63%">
Begins an enumeration of the properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d8656d7-37e5-4921-906e-c82f8878cd90">BeginMethodEnumeration</a>
</td>
<td align="left" width="63%">
Begins an enumeration of methods for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/246e5c2e-8d89-4ab5-b9ae-21a41eefa2e2">CompareTo</a>
</td>
<td align="left" width="63%">
Tests two objects for equality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01ccfad7-8529-4eb5-ae3a-cc1657022999">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified property from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75502b28-1157-4bdd-ba8f-d2cf0c1228c4">DeleteMethod</a>
</td>
<td align="left" width="63%">
Removes a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a9fa8567-7504-4d59-a874-1dc7b2620a0b">EndEnumeration</a>
</td>
<td align="left" width="63%">
Ends an enumeration begun with 
     <a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">BeginEnumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a6de467-65f7-4873-a2dd-9c52c138b1d2">EndMethodEnumeration</a>
</td>
<td align="left" width="63%">
Ends the enumeration of methods for an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>
</td>
<td align="left" width="63%">
Gets a particular property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d4775fe0-62bf-40a6-8e2c-7bc8c3d92e1f">GetMethod</a>
</td>
<td align="left" width="63%">
Gets the in- and out-parameter definitions for a specific method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3d55b1f-f9bd-40d1-9ad5-990c264524d5">GetMethodOrigin</a>
</td>
<td align="left" width="63%">
Reports the class in which a method is defined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba328f43-b08a-4b09-8aff-d7075cb6d419">GetMethodQualifierSet</a>
</td>
<td align="left" width="63%">
Returns the qualifier set object for a specific method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc75fb17-52a2-40dd-b333-fcd01cae1430">GetNames</a>
</td>
<td align="left" width="63%">
Obtains a list of the names of the properties in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7e874e9a-7417-4b3f-95c5-398fe92bfdf8">GetObjectText</a>
</td>
<td align="left" width="63%">
Obtains the textual rendition of the object in Managed Object Format (MOF) syntax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05228d88-baa2-4e89-a8c8-139f9ffea86c">GetPropertyOrigin</a>
</td>
<td align="left" width="63%">
Reports the class in which a particular property was introduced.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bfca42e-7688-42e1-afa3-24b7eaaad9fe">GetPropertyQualifierSet</a>
</td>
<td align="left" width="63%">
Allows access to the qualifiers of a particular property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da86b723-8126-44b9-95ec-120d88390ef3">GetQualifierSet</a>
</td>
<td align="left" width="63%">
Allows access to the qualifier set of the entire object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05431e05-440e-4241-bde9-0dbd32039921">InheritsFrom</a>
</td>
<td align="left" width="63%">
Reports whether the current object inherits from a particular class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Obtains the next property in an enumeration after an initial call to 
     <a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">BeginEnumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c11e043-518b-46f6-bb39-e80354ef2c8a">NextMethod</a>
</td>
<td align="left" width="63%">
Retrieves the next method definition in an enumeration of methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7b67739f-5c67-447a-a1a5-fad9ce3e857a">Put</a>
</td>
<td align="left" width="63%">
Updates or creates a particular property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eebfe049-e30e-40e0-a3bd-85a4bc11582f">PutMethod</a>
</td>
<td align="left" width="63%">
Creates a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b27c984-2261-4263-a32e-977aba5e3f06">SpawnDerivedClass</a>
</td>
<td align="left" width="63%">
Creates a new derived class from the current class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f244c1b-60ed-41ff-8464-5ac66737a5da">SpawnInstance</a>
</td>
<td align="left" width="63%">
Creates a new instance from the current class.

</td>
</tr>
</table> 


## -remarks



Users and providers should never implement this interface. The implementation provided by WMI is the only one 
     that is supported.

From the WMI client perspective, this interface is always in-process. Write 
     (<a href="https://msdn.microsoft.com/7b67739f-5c67-447a-a1a5-fad9ce3e857a">Put</a>) operations only affect the local copy of the 
     object, and read (<a href="https://msdn.microsoft.com/library/windows/hardware/jj983411">Get</a>) operations always retrieve 
     values from the local copy. You can perform updates to WMI only when entire objects are read or written using 
     methods on the <a href="https://msdn.microsoft.com/58e2ecca-7d1f-4831-93fc-f946f8ada2c0">IWbemServices</a> interface. Examples of such 
     updates are: <a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> or 
     <a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">IWbemServices::PutClass</a>.




## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/ee54c1ef-bc91-4771-8c11-9ee3aacd8112">Creating and Declaring an Instance Using C++</a>



<a href="https://msdn.microsoft.com/5ae95707-d023-4102-9b41-140c54b0c5b7">Describing a Class Object Path</a>



<a href="https://msdn.microsoft.com/78a194f0-cd21-4622-9242-be7e430b96c0">Describing an Instance Object Path</a>



<a href="https://msdn.microsoft.com/5bfd9d9b-ffe5-4def-a97d-85c4c01223f0">Making Calls to WMI</a>
 

 

