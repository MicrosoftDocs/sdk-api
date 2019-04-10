---
UID: NN:propidl.IPropertySetStorage
title: IPropertySetStorage (propidl.h)
author: windows-sdk-content
description: The IPropertySetStorage interface creates, opens, deletes, and enumerates property set storages that support instances of the IPropertyStorage interface.
old-location: stg\ipropertysetstorage.htm
tech.root: Stg
ms.assetid: 0ea3e1e0-c135-4138-81e4-f72412fc3128
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertySetStorage, IPropertySetStorage [Strctd Stg], IPropertySetStorage interface [Structured Storage], IPropertySetStorage interface [Structured Storage],described, _stg_ipropertysetstorage, propidl/IPropertySetStorage, stg.ipropertysetstorage
ms.topic: interface
req.header: propidl.h
req.include-header: Objbase.h
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
 - IPropertySetStorage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertySetStorage interface


## -description


The 
<b>IPropertySetStorage</b> interface creates, opens, deletes, and enumerates property set storages that support instances of the 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interface. The 
<b>IPropertyStorage</b> interface manages a single property set in a property storage subobject; and the 
<b>IPropertySetStorage</b> interface manages the storage of groups of such property sets. Any file system entity can support 
<b>IPropertySetStorage</b> that is currently implemented in the COM compound file object.

The 
<b>IPropertySetStorage</b> and 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> interfaces provide a uniform way to create and manage property sets, whether or not these sets reside in a storage object that supports 
<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a>. When called through an object supporting 
<b>IStorage</b> (such as structured and compound files) or 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a>, the property sets created conform to the COM property set format, described in detail in 
<a href="https://msdn.microsoft.com/f22abe40-535f-4178-9460-59bbe26ff178">Structured Storage Serialized Property Set Format</a>. Similarly, properties written using 
<b>IStorage</b> to the COM property set format are visible through 
<b>IPropertySetStorage</b> and 
<b>IPropertyStorage</b>.

<b>IPropertySetStorage</b> methods identify property sets through a globally unique identifier (GUID) called a format identifier (FMTID). The FMTID for a property set identifies the property identifiers in the property set, their meaning, and any constraints on the values. The FMTID of a property set should also provide the means to manipulate that property set. Only one instance of a given FMTID may exist at a time within a single property storage.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertySetStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertySetStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertySetStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">Create</a>
</td>
<td align="left" width="63%">
Creates a new property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c65942f-b73b-48e5-a59e-4424708a084a">Delete</a>
</td>
<td align="left" width="63%">
Deletes an existing property set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/979ee86b-fabc-428c-8134-f16c2a33270f">Enum</a>
</td>
<td align="left" width="63%">
Creates and retrieves a pointer to an object that can be used to enumerate property sets.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0e2239f-b908-460a-98e8-c805c1d84def">Open</a>
</td>
<td align="left" width="63%">
Opens a previously created property set.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  There is an exception to the above in The DocumentSummaryInformation and UserDefined property set. This property set is unique in that it may have two property set sections in a single underlying stream. This property set is described in <a href="https://msdn.microsoft.com/c6d4e2bc-f7f6-429d-aa91-432d833c69d1">The DocumentSummaryInformation and UserDefined Property Sets</a>. The first section is the DocumentSummaryInformation property set. The second section is the UserDefined property set. Each section is identified by a unique format identifier (FMTID).  For example, FMTID_DocSummaryInformation and FMTID_UserDefined property set. The fact that these two property sets can exist in a single stream affects the behavior of the <b>IPropertySetStorage</b> interface.<p class="note">When <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a> is called to create the UserDefined property set, the first section is created automatically. Once the FMTID_UserDefinedProperties is created, FMTID_DocSummaryInformation need not be created, but can be operend with a call to <a href="https://msdn.microsoft.com/a0e2239f-b908-460a-98e8-c805c1d84def">IPropertySetStorage::Open</a>. Creating the first section does not automatically create the second section and it is not possible to open both sections simultaneously.

<p class="note">Calling <a href="https://msdn.microsoft.com/5c65942f-b73b-48e5-a59e-4424708a084a">IPropertySetStorage::Delete</a>, to delete the first section, causes both sections to be deleted.  In other words, calling <b>IPropertySetStorage::Delete</b> with FMTID_DocSummaryInformation causes both that section and the FMTID_UserDefinedProperties section to be deleted. However, deleting the second section does not automatically delete the first section.

<p class="note">When <a href="https://msdn.microsoft.com/979ee86b-fabc-428c-8134-f16c2a33270f">IPropertySetStorage::Enum</a> is used to enumerate property sets, the UserDefined property set is not enumerated.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/8d5e658f-312c-4c91-8794-808b2e8dd182">IEnumSTATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/de2cb778-c6eb-4487-996b-87405674f603">IPropertySetStorage-Compound File Implementation</a>



<a href="https://msdn.microsoft.com/cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8">IPropertySetStorage-NTFS File System Implementation</a>



<a href="https://msdn.microsoft.com/0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2">IPropertySetStorage-Stand-alone Implementation</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/8e5cc502-9f96-4f4b-8729-cac4a1ffcd6f">STATPROPSETSTG</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>
 

 

