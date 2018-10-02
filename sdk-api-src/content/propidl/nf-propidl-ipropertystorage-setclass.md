---
UID: NF:propidl.IPropertyStorage.SetClass
title: IPropertyStorage::SetClass
author: windows-sdk-content
description: The SetClass method assigns a new CLSID to the current property storage object, and persistently stores the CLSID with the object.
old-location: stg\ipropertystorage_setclass.htm
tech.root: Stg
ms.assetid: 88c916e5-b7f0-4f4d-b049-df2b0e1c2423
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPropertyStorage [Strctd Stg],SetClass, IPropertyStorage interface [Structured Storage],SetClass method, IPropertyStorage.SetClass, IPropertyStorage::SetClass, SetClass, SetClass method [Structured Storage], SetClass method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_setclass, propidl/IPropertyStorage::SetClass, stg.ipropertystorage_setclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
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
 - IPropertyStorage.SetClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyStorage::SetClass


## -description


The <b>SetClass</b> method assigns a new CLSID to the current property storage object, and persistently stores the CLSID with the object.


## -parameters




### -param clsid [in]

New CLSID to be associated with the property set.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



Assigns a CLSID to the current property storage object. The CLSID has no relationship to the stored property IDs. Assigning a CLSID allows a piece of code to be associated with a given instance of a property set; such code, for example, might manage the user interface (UI). Different CLSIDs can be associated with different property set instances that have the same FMTID.

If the property set is created with the <i>pclsid</i> parameter of the <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a> method specified as <b>NULL</b>, the CLSID is set to all zeroes.

The current CLSID on a property storage object can be retrieved with a call to 
<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>. The initial value for the CLSID can be specified at the time that the storage is created with a call to <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>.

Setting the CLSID on a nonsimple property set (one that can legally contain storage- or stream-valued properties, as described in <a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>) also sets the CLSID on the underlying sub-storage.




## -see-also




<a href="https://msdn.microsoft.com/9307788d-bce6-4025-8043-8b68e874a62b">IPropertySetStorage::Create</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
 

 

