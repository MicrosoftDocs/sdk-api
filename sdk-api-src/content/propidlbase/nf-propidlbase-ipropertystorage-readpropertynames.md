---
UID: NF:propidlbase.IPropertyStorage.ReadPropertyNames
title: IPropertyStorage::ReadPropertyNames (propidlbase.h)
author: windows-sdk-content
description: Retrieves any existing string names for the specified property IDs.
old-location: stg\ipropertystorage_readpropertynames.htm
tech.root: Stg
ms.assetid: 42b0bf7e-0402-425c-8a5f-09eaa16d93fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPropertyStorage [Strctd Stg], IPropertyStorage [Strctd Stg],ReadPropertyNames, IPropertyStorage interface [Structured Storage],ReadPropertyNames method, IPropertyStorage.ReadPropertyNames, IPropertyStorage::ReadPropertyNames, ReadPropertyNames, ReadPropertyNames method [Structured Storage], ReadPropertyNames method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_readpropertynames, propidl/IPropertyStorage::ReadPropertyNames, stg.ipropertystorage_readpropertynames
ms.topic: method
req.header: propidlbase.h
req.include-header: Objbase.h, Propidlbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPropertyStorage.ReadPropertyNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyStorage::ReadPropertyNames


## -description


The <b>ReadPropertyNames</b> method retrieves any existing string names for the specified property IDs.


## -parameters




### -param cpropid [in]

The number of elements on input of the array <i>rgpropid</i>.  The value of this parameter can be set to zero, however that defeats the purpose of this method as no property names are thereby read.


### -param rgpropid [in]

An array of property IDs for which names are to be retrieved.


### -param rglpwstrName [in, out]

A caller-allocated array of size <i>cpropid</i> of <b>LPWSTR</b> members. On return, the implementation fills in this array. A given entry contains either the corresponding string name of a property ID or it can be empty if the property ID has no string names.

Each <b>LPWSTR</b> member of the array should be freed using the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



For each property ID in the list of property IDs supplied in the <i>rgpropid</i> array, <b>ReadPropertyNames</b> retrieves the corresponding string name, if there is one. String names are created either by specifying the names in calls to 
<a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a> when creating the property, or through a call to <a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>. In either case, the string name is optional, however all properties must have a property ID.

String names mapped to property IDs must be unique within the set.




## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/480a2be3-ccb0-4135-a085-733f6ab48ccd">IPropertyStorage::WriteMultiple</a>



<a href="https://msdn.microsoft.com/3612bf29-344a-4389-bd3b-56b9fa297362">IPropertyStorage::WritePropertyNames</a>
 

 

