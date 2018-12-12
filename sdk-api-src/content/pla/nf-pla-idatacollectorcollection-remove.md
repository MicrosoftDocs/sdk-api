---
UID: NF:pla.IDataCollectorCollection.Remove
title: IDataCollectorCollection::Remove
author: windows-sdk-content
description: Removes a data collector from the collection.
old-location: pla\idatacollectorcollection_remove.htm
tech.root: pla
ms.assetid: 7f5a6d20-d65a-477b-8886-8536315bc36e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorCollection interface [PLA],Remove method, IDataCollectorCollection.Remove, IDataCollectorCollection::Remove, Remove, Remove method [PLA], Remove method [PLA],IDataCollectorCollection interface, base.idatacollectorcollection_remove, pla.idatacollectorcollection_remove, pla/IDataCollectorCollection::Remove
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
 - IDataCollectorCollection.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorCollection::Remove


## -description


Removes a data collector from the collection.


## -parameters




### -param collector [in]

The zero-based index of the data collector to remove from the collection. The variant type can be VT_I4, VT_UI4, or VT_DISPATCH.


## -returns



Returns S_OK if successful.




## -remarks



If the variant type is VT_DISPATCH, pass the <b>IDispatch</b> interface of the <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> to be removed.

Note that by removing the collector from the collection, you are also removing the collector from the data collector set.




## -see-also




<a href="https://msdn.microsoft.com/6b47fb9d-6ca4-4e6b-b117-027ef1e963ac">IDataCollectorCollection</a>



<a href="https://msdn.microsoft.com/6302e144-74ef-4251-a857-d3e066c9763d">IDataCollectorCollection::Add</a>



<a href="https://msdn.microsoft.com/be0840dc-e19a-454e-bbea-6968c7284cc8">IDataCollectorCollection::Clear</a>
 

 

