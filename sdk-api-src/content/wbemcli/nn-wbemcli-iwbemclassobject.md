---
UID: NN:wbemcli.IWbemClassObject
title: IWbemClassObject (wbemcli.h)
description: Contains and manipulates both class definitions and class object instances.
helpviewer_keywords: ["IWbemClassObject","IWbemClassObject interface [Windows Management Instrumentation]","IWbemClassObject interface [Windows Management Instrumentation]","described","WbemClassObject","_hmm_iwbemclassobject","wbemcli/IWbemClassObject","wmi.iwbemclassobject"]
old-location: wmi\iwbemclassobject.htm
tech.root: wmi
ms.assetid: a3ce37d7-5580-4b84-9119-78412c8e0d27
ms.date: 12/05/2018
ms.keywords: IWbemClassObject, IWbemClassObject interface [Windows Management Instrumentation], IWbemClassObject interface [Windows Management Instrumentation],described, WbemClassObject, _hmm_iwbemclassobject, wbemcli/IWbemClassObject, wmi.iwbemclassobject
f1_keywords:
- wbemcli/IWbemClassObject
dev_langs:
- c++
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
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- CIMWin32.dll
- Esscli.dll
- Fastprox.dll
- FrameDyn.dll
- FrameDynOS.dll
- Krnlprov.dll
- Ncprov.dll
- Wbemcore.dll
- Wbemess.dll
- Wmipiprt.dll
api_name:
- IWbemClassObject
- WbemClassObject
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemClassObject interface


## -description


The <b>IWbemClassObject</b> interface 
    contains and manipulates both class definitions and class object instances.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemClassObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemClassObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">BeginEnumeration</a>
</td>
<td align="left" width="63%">
Begins an enumeration of the properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginmethodenumeration">BeginMethodEnumeration</a>
</td>
<td align="left" width="63%">
Begins an enumeration of methods for the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the current object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-compareto">CompareTo</a>
</td>
<td align="left" width="63%">
Tests two objects for equality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-delete">Delete</a>
</td>
<td align="left" width="63%">
Removes the specified property from the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-deletemethod">DeleteMethod</a>
</td>
<td align="left" width="63%">
Removes a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endenumeration">EndEnumeration</a>
</td>
<td align="left" width="63%">
Ends an enumeration begun with 
     <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">BeginEnumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endmethodenumeration">EndMethodEnumeration</a>
</td>
<td align="left" width="63%">
Ends the enumeration of methods for an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">Get</a>
</td>
<td align="left" width="63%">
Gets a particular property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethod">GetMethod</a>
</td>
<td align="left" width="63%">
Gets the in- and out-parameter definitions for a specific method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethodorigin">GetMethodOrigin</a>
</td>
<td align="left" width="63%">
Reports the class in which a method is defined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getmethodqualifierset">GetMethodQualifierSet</a>
</td>
<td align="left" width="63%">
Returns the qualifier set object for a specific method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getnames">GetNames</a>
</td>
<td align="left" width="63%">
Obtains a list of the names of the properties in the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext">GetObjectText</a>
</td>
<td align="left" width="63%">
Obtains the textual rendition of the object in Managed Object Format (MOF) syntax.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyorigin">GetPropertyOrigin</a>
</td>
<td align="left" width="63%">
Reports the class in which a particular property was introduced.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset">GetPropertyQualifierSet</a>
</td>
<td align="left" width="63%">
Allows access to the qualifiers of a particular property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getqualifierset">GetQualifierSet</a>
</td>
<td align="left" width="63%">
Allows access to the qualifier set of the entire object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-inheritsfrom">InheritsFrom</a>
</td>
<td align="left" width="63%">
Reports whether the current object inherits from a particular class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-next">Next</a>
</td>
<td align="left" width="63%">
Obtains the next property in an enumeration after an initial call to 
     <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">BeginEnumeration</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-nextmethod">NextMethod</a>
</td>
<td align="left" width="63%">
Retrieves the next method definition in an enumeration of methods.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put">Put</a>
</td>
<td align="left" width="63%">
Updates or creates a particular property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-putmethod">PutMethod</a>
</td>
<td align="left" width="63%">
Creates a method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawnderivedclass">SpawnDerivedClass</a>
</td>
<td align="left" width="63%">
Creates a new derived class from the current class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawninstance">SpawnInstance</a>
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
     (<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put">Put</a>) operations only affect the local copy of the 
     object, and read (<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">Get</a>) operations always retrieve 
     values from the local copy. You can perform updates to WMI only when entire objects are read or written using 
     methods on the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> interface. Examples of such 
     updates are: <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> or 
     <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putclass">IWbemServices::PutClass</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/creating-and-declaring-an-instance-using-c-">Creating and Declaring an Instance Using C++</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/describing-a-class-object-path">Describing a Class Object Path</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/describing-an-instance-object-path">Describing an Instance Object Path</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>
 

 

