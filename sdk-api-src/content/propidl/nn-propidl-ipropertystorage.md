---
UID: NN:propidl.IPropertyStorage
title: IPropertyStorage (propidl.h)
description: The IPropertyStorage interface manages the persistent properties of a single property set. (IPropertyStorage interface)
helpviewer_keywords: ["IPropertyStorage","IPropertyStorage interface [Structured Storage]","IPropertyStorage interface [Structured Storage]","described","_stg_ipropertystorage","propidl/IPropertyStorage","stg.ipropertystorage"]
old-location: stg\ipropertystorage.htm
tech.root: Stg
ms.assetid: c021f695-db54-4861-9f30-35a81d2dccd5
ms.date: 08/02/2022
ms.keywords: IPropertyStorage, IPropertyStorage interface [Structured Storage], IPropertyStorage interface [Structured Storage],described, _stg_ipropertystorage, propidl/IPropertyStorage, stg.ipropertystorage
req.header: propidl.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyStorage
 - propidl/IPropertyStorage
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
 - IPropertyStorage
---

# IPropertyStorage interface


## -description

The <b>IPropertyStorage</b> interface manages the persistent properties of a single property set. Persistent properties consist of information that can be stored persistently in a property set, such as the summary information associated with a file. This contrasts with run-time properties associated with Controls and Automation, which can be used to affect system behavior. Use the methods of the 
<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a> interface to create or open a persistent property set. An instance of the 
<b>IPropertySetStorage</b> interface can manage zero or more 
<b>IPropertyStorage</b> instances.

Each property within a property set is identified by a property identifier (ID), a four-byte <b>ULONG</b> value unique to that set. You can also assign a string name to a property through the 
<b>IPropertyStorage</b> interface.

Property IDs differ from the dispatch IDs used in Automation <b>dispid</b> property name tags. One difference is that the general-purpose use of property ID values zero and one is prohibited in 
<b>IPropertyStorage</b>, while no such restriction exists in <b>IDispatch</b>. In addition, while there is significant overlap among the data types for property values that may be used in 
<b>IPropertyStorage</b> and <b>IDispatch</b>, the property sets are not identical. Persistent property data types used in 
<b>IPropertyStorage</b> methods are defined in the 
<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

The 
<b>IPropertyStorage</b> interface can be used to access both simple and nonsimple property sets. Nonsimple property sets can hold several complex property types that cannot be held in a simple property set. For more information see 
<a href="/windows/desktop/Stg/storage-vs--stream-for-a-property-set">Storage and Stream Objects for a Property Set</a>.

## -inheritance

The <b>IPropertyStorage</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyStorage</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropsetstg">IEnumSTATPROPSETSTG</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ienumstatpropstg">IEnumSTATPROPSTG</a>



<a href="/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage">IPropertySetStorage</a>



<a href="/windows/desktop/Stg/ipropertystorage-compound-file-implementation">IPropertyStorage-Compound File Implementation</a>



<a href="/windows/desktop/Stg/ipropertystorage-ntfs-file-system-implementation">IPropertyStorage-NTFS File System Implementation</a>



<a href="/windows/desktop/Stg/ipropertystorage-stand-alone-implementation">IPropertyStorage-Stand-alone Implementation</a>



<a href="/windows/desktop/Stg/managing-properties">Managing
		  Properties</a>



<a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>



<a href="/windows/desktop/Stg/property-storage-considerations">Property
		  Storage Considerations</a>



<a href="/windows/desktop/api/propidl/ns-propidl-statpropsetstg">STATPROPSETSTG</a>



<a href="/windows/desktop/api/propidl/ns-propidl-statpropstg">STATPROPSTG</a>



<a href="/windows/desktop/Stg/samples">Samples</a>
