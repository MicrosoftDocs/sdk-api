---
UID: NN:propidl.IPropertyStorage
title: IPropertyStorage
author: windows-sdk-content
description: The IPropertyStorage interface manages the persistent properties of a single property set.
old-location: stg\ipropertystorage.htm
old-project: Stg
ms.assetid: c021f695-db54-4861-9f30-35a81d2dccd5
ms.author: windowssdkdev
ms.date: 06/06/2018
ms.keywords: IPropertyStorage, IPropertyStorage interface [Structured Storage], IPropertyStorage interface [Structured Storage],described, _stg_ipropertystorage, propidl/IPropertyStorage, stg.ipropertystorage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IPropertyStorage interface


## -description


The <b>IPropertyStorage</b> interface manages the persistent properties of a single property set. Persistent properties consist of information that can be stored persistently in a property set, such as the summary information associated with a file. This contrasts with run-time properties associated with Controls and Automation, which can be used to affect system behavior. Use the methods of the 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a> interface to create or open a persistent property set. An instance of the 
<b>IPropertySetStorage</b> interface can manage zero or more 
<b>IPropertyStorage</b> instances.

Each property within a property set is identified by a property identifier (ID), a four-byte <b>ULONG</b> value unique to that set. You can also assign a string name to a property through the 
<b>IPropertyStorage</b> interface.

Property IDs differ from the dispatch IDs used in Automation <b>dispid</b> property name tags. One difference is that the general-purpose use of property ID values zero and one is prohibited in 
<b>IPropertyStorage</b>, while no such restriction exists in <b>IDispatch</b>. In addition, while there is significant overlap among the data types for property values that may be used in 
<b>IPropertyStorage</b> and <b>IDispatch</b>, the property sets are not identical. Persistent property data types used in 
<b>IPropertyStorage</b> methods are defined in the 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.

The 
<b>IPropertyStorage</b> interface can be used to access both simple and nonsimple property sets. Nonsimple property sets can hold several complex property types that cannot be held in a simple property set. For more information see 
<a href="https://msdn.microsoft.com/d0ca649a-d405-4c34-af02-9c2ca8b2790e">Storage and Stream Objects for a Property Set</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertyStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertyStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
As in <a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>, flushes or commits changes to the property storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c218f1-2bf7-4946-ae9c-934e5916395a">DeleteMultiple</a>
</td>
<td align="left" width="63%">
Deletes properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fedeb7fb-b84a-44a4-82d8-3a365296af69">DeletePropertyNames</a>
</td>
<td align="left" width="63%">
Deletes string names for given property identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73f834cf-b6e4-4a48-bbdc-0c4ba87aacaf">Enum</a>
</td>
<td align="left" width="63%">
Creates and gets a pointer to an enumerator for properties within this set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">ReadMultiple</a>
</td>
<td align="left" width="63%">
Reads property values in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42b0bf7e-0402-425c-8a5f-09eaa16d93fe">ReadPropertyNames</a>
</td>
<td align="left" width="63%">
Gets corresponding string names for given property identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31e0d3e7-8575-4788-b42e-606221cf5a4c">Revert</a>
</td>
<td align="left" width="63%">
When the property storage is opened in transacted mode, discards all changes since the last commit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/88c916e5-b7f0-4f4d-b049-df2b0e1c2423">SetClass</a>
</td>
<td align="left" width="63%">
Assigns a CLSID to the property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23c7040a-e648-4898-806d-ad01d7027cc6">SetTimes</a>
</td>
<td align="left" width="63%">
Sets modification, creation, and access times for the property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">Stat</a>
</td>
<td align="left" width="63%">
Receives statistics about this property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">WriteMultiple</a>
</td>
<td align="left" width="63%">
Writes property values in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">WritePropertyNames</a>
</td>
<td align="left" width="63%">
Creates or changes string names corresponding to given property identifiers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/e625e52a-5628-4d18-9282-aa1c141c83af">IEnumSTATPROPSTG</a>



<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>



<a href="https://msdn.microsoft.com/c4b4f313-de58-44f2-8ce1-a07cc187d8ca">IPropertyStorage-Compound File Implementation</a>



<a href="https://msdn.microsoft.com/d0ffd975-5bc2-4de3-b0c1-c9188541f46a">IPropertyStorage-NTFS File System Implementation</a>



<a href="https://msdn.microsoft.com/8de32538-de11-4e4d-9269-145b2accb099">IPropertyStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/d220ecb4-b014-4ac9-a636-9a493187cc87">Managing
		  Properties</a>



<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/7540966f-a3b2-46c9-9e04-b15133a517eb">Property
		  Storage Considerations</a>



<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/3b8de6d3-18a3-4c0a-94d1-04bcec05d41a">STATPROPSTG</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

