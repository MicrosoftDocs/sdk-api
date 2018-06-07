---
UID: NF:propidl.IPropertyStorage.WriteMultiple
title: IPropertyStorage::WriteMultiple
author: windows-sdk-content
description: Writes a specified group of properties to the current property set.
old-location: stg\ipropertystorage_writemultiple.htm
old-project: Stg
ms.assetid: 480a2be3-ccb0-4135-a085-733f6ab48ccd
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IPropertyStorage interface [Structured Storage],WriteMultiple method, IPropertyStorage.WriteMultiple, IPropertyStorage::WriteMultiple, WriteMultiple, WriteMultiple method [Structured Storage], WriteMultiple method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_writemultiple, propidl/IPropertyStorage::WriteMultiple, stg.ipropertystorage_writemultiple
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPropertyStorage.WriteMultiple
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPropertyStorage::WriteMultiple


## -description


The 
<b>WriteMultiple</b> method 
			writes a specified group of properties to the current property set. If a property with a specified name or property identifier already exists, it is replaced, even when the old and new types for the property value are different. If a property of a given name or property ID does not exist, it is created.


## -parameters




### -param cpspec [in]

The number of properties set. The value of this parameter can be set to zero; however, this defeats the purpose of the method as no properties are then written.


### -param rgpspec [in]

An array of the property IDs (<a href="https://msdn.microsoft.com/5bb3b9c6-ab82-498c-94f9-13a9ffa7452b">PROPSPEC</a>) to which properties are set. These need not be in any particular order, and may contain duplicates, however the last specified property ID is the one that takes effect. A mixture of property IDs and string names is permitted.


### -param rgpropvar [in]

An array (of size <i>cpspec</i>) of 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures that contain the property values to be written. The array must be the size specified by <i>cpspec</i>.


### -param propidNameFirst [in]

The minimum value for the property IDs that the method must assign if the <i>rgpspec</i> parameter specifies string-named properties for which no property IDs currently exist. If all string-named properties specified already exist in this set, and thus already have property IDs, this value is ignored. When not ignored, this value must be greater than, or equal to, two and less than 0x80000000. Property IDs 0 and 1 and greater than 0x80000000 are reserved for special use.


## -returns




						This method supports the standard return value E_UNEXPECTED, in addition to the following:

This function can also return any file system errors or Win32 errors wrapped in an <b>HRESULT</b> data type. For more information, see 
<a href="https://docs.microsoft.com/windows/desktop//com/error-handling-strategies">Error Handling Strategies</a>.




## -remarks



If a specified property already exists, its value is replaced with the one specified in <i>rgpspec</i>, even when the old and new types for the property value are different. If the specified property does not already exist, that property is created. The changes are not persisted to the underlying storage until <a href="https://msdn.microsoft.com/00efae8b-023e-425d-b7cd-c40c17d7948e">IPropertyStorage::Commit</a> has been called.

Property names are stored in a special dictionary section of the property set, which maps such names to property IDs. All properties have an ID, but names are optional. A string name is supplied by specifying PRSPEC_LPWSTR in the <b>ulKind</b> member of the 
<a href="https://msdn.microsoft.com/5bb3b9c6-ab82-498c-94f9-13a9ffa7452b">PROPSPEC</a> structure. If a string name is supplied for a property, and the name does not already exist in the dictionary, the method will allocate a property ID, and add the property ID and the name to the dictionary. The property ID is allocated in such a way that it does not conflict with other IDs in the property set. The value of the property ID also is no less than the value specified by the <i>propidNameFirst</i> parameter. If the <i>rgpspec</i> parameter specifies string-named properties for which no property IDs currently exist, the <i>propidNameFirst</i> parameter specifies the minimum value for the property IDs that the 
<b>WriteMultiple</b> method must assign.

When a new property set is created, the special <b>codepage (</b><a href="https://msdn.microsoft.com/">Property ID 1</a><b>)</b> and <b>Locale ID (</b><a href="https://msdn.microsoft.com/">Property ID 0x80000000</a><b>)</b> properties are written to the property set automatically. These properties can subsequently be read, using the <a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">IPropertyStorage::ReadMultiple</a> method, by specifying property IDs with the header-defined PID_CODEPAGE and PID_LOCALE values, respectively. If a property set is non-empty — has one or more properties in addition to the <b>codepage</b> and <b>Locale ID</b> properties or has one or more names in its dictionary — the special <b>codepage</b> and <b>Locale ID</b> properties cannot be modified by calling <b>IPropertyStorage::WriteMultiple</b>. However, if the property set is empty, one or both of these special properties can be modified.

If an element in the <i>rgspec</i> array is set with a PRSPEC_PROPID value of 0xffffffff (PID_ILLEGAL), the corresponding value in the <i>rgvar</i> array is ignored by <b>IPropertyStorage::WriteMultiple</b>. For example, if this method is called with the <i>cspec</i> parameter set to 3, but <i>rgpspec[1].prspec</i> is set to PRSPEC_PROPID and <i>rgpspec[1].propid</i> is set to PID_ILLEGAL, only two properties will be written. The <i>rgpropvar[1]</i> element is silently ignored.

Use the 
<a href="https://msdn.microsoft.com/8c1bf6ac-2b15-4a05-8cb9-a07d1437017c">PropVariantInit</a> macro to initialize 
<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures.

Property sets, not including the data for nonsimple properties, are limited to 256 KB in size for Windows NT 4.0 and earlier. For Windows 2000, Windows XP and Windows Server 2003, OLE property sets are limited to 1 MB.  If these limits are exceeded, the operation fails and the caller receives an error message. There is no possibility of a memory leak or overrun. For more information, see 
<a href="https://msdn.microsoft.com/19ff2751-87f3-43d8-9307-ce2dd399f694">Managing Property Sets</a>.

Unless PROPSETFLAG_CASE_SENSITIVE is passed to <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>, property set names are case insensitive. Specifying a property by its name in <b>IPropertyStorage::WriteMultiple</b> will result in a case-insensitive search of the names in the property set. To compare case-insensitive strings, the locale of the strings must be known. For more information, see 
<a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>.

For more information, see 
<a href="https://msdn.microsoft.com/7540966f-a3b2-46c9-9e04-b15133a517eb">Property Storage Considerations</a>.




## -see-also




<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>



<a href="https://msdn.microsoft.com/a3d708fe-53af-4f1b-94ac-edc40d59a034">IPropertyStorage::ReadMultiple</a>



<a href="https://msdn.microsoft.com/19ff2751-87f3-43d8-9307-ce2dd399f694">Managing Property Sets</a>



<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>



<a href="https://msdn.microsoft.com/0c48da47-b718-48fe-8ad0-39686bb83283">Samples</a>



<a href="https://msdn.microsoft.com/f0d0664a-2cfd-4eb0-b1d5-47d1545394fd">StgCreatePropSetStg Sample</a>



<a href="https://msdn.microsoft.com/c5807dd9-2928-497b-9446-729dcaeebc8a">WriteRead Sample</a>
 

 

