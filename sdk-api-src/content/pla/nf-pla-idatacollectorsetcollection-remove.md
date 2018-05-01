---
UID: NF:pla.IDataCollectorSetCollection.Remove
title: IDataCollectorSetCollection::Remove method
author: windows-driver-content
description: Removes a data collector set from the collection.
old-location: pla\idatacollectorsetcollection_remove.htm
old-project: PLA
ms.assetid: 6200dac0-8817-4d59-9456-67921bcf15ae
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataCollectorSetCollection, IDataCollectorSetCollection interface [PLA], Remove method, IDataCollectorSetCollection::Remove, Remove method [PLA], Remove method [PLA], IDataCollectorSetCollection interface, Remove,IDataCollectorSetCollection.Remove, base.idatacollectorsetcollection_remove, pla.idatacollectorsetcollection_remove, pla/IDataCollectorSetCollection::Remove
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
-	IDataCollectorSetCollection.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IDataCollectorSetCollection::Remove method


## -description


Removes a data collector set from the collection.


## -parameters




### -param set






#### - vSet [in]

The zero-based index of the data collector set to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a> to be removed.

Note that by removing the set from the collection, you are also deleting the set from the hard disk.




## -see-also




<a href="https://msdn.microsoft.com/5f4cc411-1efb-4f70-a677-3c20d95f0c53">IDataCollectorSetCollection</a>



<a href="https://msdn.microsoft.com/c551e373-77a4-4bac-848d-5aaec1e89cf1">IDataCollectorSetCollection::Add</a>



<a href="https://msdn.microsoft.com/a7a4754c-8c64-4add-89b1-c5bdbf4cb807">IDataCollectorSetCollection::Clear</a>
 

 

