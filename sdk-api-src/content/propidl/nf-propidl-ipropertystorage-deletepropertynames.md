---
UID: NF:propidl.IPropertyStorage.DeletePropertyNames
title: IPropertyStorage::DeletePropertyNames
author: windows-sdk-content
description: The DeletePropertyNames method deletes specified string names from the current property set.
old-location: stg\ipropertystorage_deletepropertynames.htm
old-project: stg
ms.assetid: fedeb7fb-b84a-44a4-82d8-3a365296af69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DeletePropertyNames, DeletePropertyNames method [Structured Storage], DeletePropertyNames method [Structured Storage],IPropertyStorage interface, IPropertyStorage [Strctd Stg],DeletePropertyNames, IPropertyStorage interface [Structured Storage],DeletePropertyNames method, IPropertyStorage.DeletePropertyNames, IPropertyStorage::DeletePropertyNames, _stg_ipropertystorage_deletepropertynames, propidl/IPropertyStorage::DeletePropertyNames, stg.ipropertystorage_deletepropertynames
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.redist: 
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
 - IPropertyStorage.DeletePropertyNames
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: ADAM
---

# IPropertyStorage::DeletePropertyNames


## -description


The <b>DeletePropertyNames</b> method deletes specified string names from the current property set.


## -parameters




### -param cpropid [in]

The size on input of the array <i>rgpropid</i>. If 0, no property names are deleted.


### -param rgpropid [in]

Property identifiers for which string names are to be deleted.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



For each property identifier in <i>rgpropid</i>, <b>IPropertyStorage::DeletePropertyNames</b> removes any corresponding name-to-property ID mapping. An attempt is silently ignored to delete the name of a property that either does not exist or does not currently have a string name associated with it. This method has no effect on the properties themselves.

<div class="alert"><b>Note</b>  All the stored string property names can be deleted by deleting property identifier zero, but <i>cpropid</i> must be equal to 1 for this to be a valid parameter error.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/42b0bf7e-0402-425c-8a5f-09eaa16d93fe">IPropertyStorage::ReadPropertyNames</a>
 

 

