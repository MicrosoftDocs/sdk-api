---
UID: NN:propidlbase.IPropertyStorage
title: IPropertyStorage (propidlbase.h)
author: windows-sdk-content
description: The IPropertyStorage interface manages the persistent properties of a single property set.
old-location: stg\ipropertystorage.htm
tech.root: Stg
ms.assetid: c021f695-db54-4861-9f30-35a81d2dccd5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyStorage, IPropertyStorage interface [Structured Storage], IPropertyStorage interface [Structured Storage],described, _stg_ipropertystorage, propidl/IPropertyStorage, stg.ipropertystorage
ms.topic: interface
f1_keywords: 
 - "propidlbase/IPropertyStorage"
req.header: propidlbase.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStorage interface


## -description


The <b>IPropertyStorage</b> interface manages the persistent properties of a single property set. Persistent properties consist of information that can be stored persistently in a property set, such as the summary information associated with a file. This contrasts with run-time properties associated with Controls and Automation, which can be used to affect system behavior. Use the methods of the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface to create or open a persistent property set. An instance of the 
<b>IPropertySetStorage</b> interface can manage zero or more 
<b>IPropertyStorage</b> instances.

Each property within a property set is identified by a property identifier (ID), a four-byte <b>ULONG</b> value unique to that set. You can also assign a string name to a property through the 
<b>IPropertyStorage</b> interface.

Property IDs differ from the dispatch IDs used in Automation <b>dispid</b> property name tags. One difference is that the general-purpose use of property ID values zero and one is prohibited in 
<b>IPropertyStorage</b>, while no such restriction exists in <b>IDispatch</b>. In addition, while there is significant overlap among the data types for property values that may be used in 
<b>IPropertyStorage</b> and <b>IDispatch</b>, the property sets are not identical. Persistent property data types used in 
<b>IPropertyStorage</b> methods are defined in the 
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.

The 
<b>IPropertyStorage</b> interface can be used to access both simple and nonsimple property sets. Nonsimple property sets can hold several complex property types that cannot be held in a simple property set. For more information see 
<a href="https://docs.microsoft.com/windows/desktop/Stg/storage-vs--stream-for-a-property-set">Storage and Stream Objects for a Property Set</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertyStorage</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyStorage</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-commit">Commit</a>
</td>
<td align="left" width="63%">
As in <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nf-objidl-istorage-commit">IStorage::Commit</a>, flushes or commits changes to the property storage object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-deletemultiple">DeleteMultiple</a>
</td>
<td align="left" width="63%">
Deletes properties in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-deletepropertynames">DeletePropertyNames</a>
</td>
<td align="left" width="63%">
Deletes string names for given property identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-enum">Enum</a>
</td>
<td align="left" width="63%">
Creates and gets a pointer to an enumerator for properties within this set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readmultiple">ReadMultiple</a>
</td>
<td align="left" width="63%">
Reads property values in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-readpropertynames">ReadPropertyNames</a>
</td>
<td align="left" width="63%">
Gets corresponding string names for given property identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-revert">Revert</a>
</td>
<td align="left" width="63%">
When the property storage is opened in transacted mode, discards all changes since the last commit.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-setclass">SetClass</a>
</td>
<td align="left" width="63%">
Assigns a CLSID to the property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-settimes">SetTimes</a>
</td>
<td align="left" width="63%">
Sets modification, creation, and access times for the property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-stat">Stat</a>
</td>
<td align="left" width="63%">
Receives statistics about this property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writemultiple">WriteMultiple</a>
</td>
<td align="left" width="63%">
Writes property values in a property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nf-propidl-ipropertystorage-writepropertynames">WritePropertyNames</a>
</td>
<td align="left" width="63%">
Creates or changes string names corresponding to given property identifiers.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ipropertystorage-compound-file-implementation">IPropertyStorage-Compound File Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ipropertystorage-ntfs-file-system-implementation">IPropertyStorage-NTFS File System Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/ipropertystorage-stand-alone-implementation">IPropertyStorage-Stand-alone Implementation</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/managing-properties">Managing
		  Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/property-storage-considerations">Property
		  Storage Considerations</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagstatpropsetstg">STATPROPSETSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagstatpropstg">STATPROPSTG</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/samples">Samples</a>
 

 

