---
UID: NF:pla.IDataCollectorSetCollection.get__NewEnum
title: IDataCollectorSetCollection::get__NewEnum
author: windows-sdk-content
description: Retrieves an interface to the enumeration.
old-location: pla\idatacollectorsetcollection__newenum.htm
tech.root: pla
ms.assetid: f875038d-8b66-44b2-b28e-211f08a691ec
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorSetCollection interface [PLA],_NewEnum property, IDataCollectorSetCollection._NewEnum, IDataCollectorSetCollection.get__NewEnum, IDataCollectorSetCollection::_NewEnum, IDataCollectorSetCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA],IDataCollectorSetCollection interface, get__NewEnum, pla.idatacollectorsetcollection__newenum, pla/IDataCollectorSetCollection::_NewEnum, pla/IDataCollectorSetCollection::get__NewEnum
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSetCollection._NewEnum
 - IDataCollectorSetCollection.get__NewEnum
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSetCollection::get__NewEnum


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



C++ programmers use this property.

The enumeration is a snapshot of the collection at the time of the call.

The items of the enumeration are variants whose type is VT_UNKNOWN.  To query for the <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a> interface, use the <b>punkVal</b> member of the variant.




## -see-also




<a href="https://msdn.microsoft.com/5f4cc411-1efb-4f70-a677-3c20d95f0c53">IDataCollectorSetCollection</a>
 

 

