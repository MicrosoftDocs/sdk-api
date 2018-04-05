---
UID: NF:pla.IDataCollectorCollection.get__NewEnum
title: IDataCollectorCollection::get__NewEnum method
author: windows-driver-content
description: Retrieves an interface to the enumeration.
old-location: pla\idatacollectorcollection__newenum.htm
old-project: PLA
ms.assetid: 05b97d37-9ccc-4856-a71a-77dd99eab8c2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataCollectorCollection, IDataCollectorCollection interface [PLA], _NewEnum property, IDataCollectorCollection._NewEnum, IDataCollectorCollection::get__NewEnum, _NewEnum property [PLA], _NewEnum property [PLA], IDataCollectorCollection interface, get__NewEnum,IDataCollectorCollection.get__NewEnum, pla.idatacollectorcollection__newenum, pla/IDataCollectorCollection::_NewEnum, pla/IDataCollectorCollection::get__NewEnum
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorCollection._NewEnum
-	IDataCollectorCollection.get__NewEnum
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IDataCollectorCollection::get__NewEnum method


## -description


Retrieves an interface to the enumeration.

This property is read-only.


## -parameters


## -remarks



C++ programmers use this property.

The items of the enumeration are variants whose type is VT_UNKNOWN. To query for the <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> interface, use the <b>punkVal</b> member of the variant.

The enumeration is a snapshot of the collection at the time of the call.




## -see-also




<a href="https://msdn.microsoft.com/6b47fb9d-6ca4-4e6b-b117-027ef1e963ac">IDataCollectorCollection</a>
 

 

