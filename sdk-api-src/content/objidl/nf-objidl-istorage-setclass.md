---
UID: NF:objidl.IStorage.SetClass
title: IStorage::SetClass method
author: windows-driver-content
description: The SetClass method assigns the specified class identifier (CLSID) to this storage object.
old-location: stg\istorage_setclass.htm
old-project: Stg
ms.assetid: 02ab2708-fc8b-4941-939a-a819cf823108
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: IStorage, IStorage interface [Structured Storage], SetClass method, IStorage::SetClass, SetClass method [Structured Storage], SetClass method [Structured Storage], IStorage interface, SetClass,IStorage.SetClass, _stg_istorage_setclass, objidl/IStorage::SetClass, stg.istorage_setclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IStorage.SetClass
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IStorage::SetClass method


## -description


The <b>SetClass</b> method assigns the specified class identifier (CLSID) to this storage object.


## -parameters




### -param clsid [in]

The CLSID that is to be associated with the storage object.


## -returns



This method can return one of these values.




## -remarks



When first created, a storage object has an associated CLSID of CLSID_NULL. Call <b>SetClass</b> to assign a CLSID to the storage object.

Call the 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a> method to retrieve the current CLSID of a storage object.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

