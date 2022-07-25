---
UID: NN:propidl.IPropertySetStorage
title: IPropertySetStorage (propidl.h)
description: The IPropertySetStorage interface creates, opens, deletes, and enumerates property set storages that support instances of the IPropertyStorage interface.
helpviewer_keywords: ["IPropertySetStorage","IPropertySetStorage [Strctd Stg]","IPropertySetStorage interface [Structured Storage]","IPropertySetStorage interface [Structured Storage]","described","_stg_ipropertysetstorage","propidl/IPropertySetStorage","stg.ipropertysetstorage"]
old-location: stg\ipropertysetstorage.htm
tech.root: Stg
ms.assetid: 0ea3e1e0-c135-4138-81e4-f72412fc3128
ms.date: 12/05/2018
ms.keywords: IPropertySetStorage, IPropertySetStorage [Strctd Stg], IPropertySetStorage interface [Structured Storage], IPropertySetStorage interface [Structured Storage],described, _stg_ipropertysetstorage, propidl/IPropertySetStorage, stg.ipropertysetstorage
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertySetStorage
 - propidl/IPropertySetStorage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertySetStorage
---

# IPropertySetStorage interface


## -description

The 
<b>IPropertySetStorage</b> interface creates, opens, deletes, and enumerates property set storages that support instances of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interface. The 
<b>IPropertyStorage</b> interface manages a single property set in a property storage subobject; and the 
<b>IPropertySetStorage</b> interface manages the storage of groups of such property sets. Any file system entity can support 
<b>IPropertySetStorage</b> that is currently implemented in the COM compound file object.

The 
<b>IPropertySetStorage</b> and 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a> interfaces provide a uniform way to create and manage property sets, whether or not these sets reside in a storage object that supports 
<a href="/windows/desktop/api/objidl/nn-objidl-istorage">IStorage</a>. When called through an object supporting 
<b>IStorage</b> (such as structured and compound files) or 
<a href="/windows/desktop/api/objidl/nn-objidl-istream">IStream</a>, the property sets created conform to the COM property set format, described in detail in 
<a href="/windows/desktop/Stg/structured-storage-serialized-property-set-format">Structured Storage Serialized Property Set Format</a>. Similarly, properties written using 
<b>IStorage</b> to the COM property set format are visible through 
<b>IPropertySetStorage</b> and 
<b>IPropertyStorage</b>.

<b>IPropertySetStorage</b> methods identify property sets through a globally unique identifier (GUID) called a format identifier (FMTID). The FMTID for a property set identifies the property identifiers in the property set, their meaning, and any constraints on the values. The FMTID of a property set should also provide the means to manipulate that property set. Only one instance of a given FMTID may exist at a time within a single property storage.

## -inheritance

The <b>IPropertySetStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertySetStorage</b> also has these types of members:

## -remarks

<div class="alert"><b>Note</b>  There is an exception to the above in The DocumentSummaryInformation and UserDefined property set. This property set is unique in that it may have two property set sections in a single underlying stream. This property set is described in <a href="/windows/desktop/Stg/the-documentsummaryinformation-and-userdefined-property-sets">The DocumentSummaryInformation and UserDefined Property Sets</a>. The first section is the DocumentSummaryInformation property set. The second section is the UserDefined property set. Each section is identified by a unique format identifier (FMTID).  For example, FMTID_DocSummaryInformation and FMTID_UserDefined property set. The fact that these two property sets can exist in a single stream affects the behavior of the <b>IPropertySetStorage</b> interface.<p class="note">When <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-create">IPropertySetStorage::Create</a> is called to create the UserDefined property set, the first section is created automatically. Once the FMTID_UserDefinedProperties is created, FMTID_DocSummaryInformation need not be created, but can be opened with a call to <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-open">IPropertySetStorage::Open</a>. Creating the first section does not automatically create the second section and it is not possible to open both sections simultaneously.

<p class="note">Calling <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-delete">IPropertySetStorage::Delete</a>, to delete the first section, causes both sections to be deleted.  In other words, calling <b>IPropertySetStorage::Delete</b> with FMTID_DocSummaryInformation causes both that section and the FMTID_UserDefinedProperties section to be deleted. However, deleting the second section does not automatically delete the first section.

<p class="note">When <a href="/windows/desktop/api/propidl/nf-propidl-ipropertysetstorage-enum">IPropertySetStorage::Enum</a> is used to enumerate property sets, the UserDefined property set is not enumerated.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/Stg/enumall-sample">EnumAll Sample</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a>



<a href="/windows/desktop/Stg/ipropertysetstorage-compound-file-implementation">IPropertySetStorage-Compound File Implementation</a>



<a href="/windows/desktop/Stg/ipropertysetstorage-ntfs-file-system-implementation">IPropertySetStorage-NTFS File System Implementation</a>



<a href="/windows/desktop/Stg/ipropertysetstorage-stand-alone-implementation">IPropertySetStorage-Stand-alone Implementation</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a>



<a href="/windows/desktop/Stg/samples">Samples</a>
