---
UID: NF:pla.IDataCollectorCollection.Add
title: IDataCollectorCollection::Add (pla.h)
author: windows-sdk-content
description: Adds a data collector to the collection.
old-location: pla\idatacollectorcollection_add.htm
tech.root: PLA
ms.assetid: 6302e144-74ef-4251-a857-d3e066c9763d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],Add method, IDataCollectorCollection.Add, IDataCollectorCollection::Add, base.idatacollectorcollection_add, pla.idatacollectorcollection_add, pla/IDataCollectorCollection::Add
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
 - IDataCollectorCollection.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorCollection::Add


## -description


Adds a data collector to the collection.


## -parameters




### -param collector [in]

An <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> interface of the data collector to add to this collection.


## -returns



Returns S_OK if successful. The following table shows a possible error value.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PLA_E_DCS_SINGLETON_REQUIRED</b></dt>
<dt>0x80300102</dt>
</dl>
</td>
<td width="60%">
The current configuration for the data collector set requires that it contain exactly one data collector.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b47fb9d-6ca4-4e6b-b117-027ef1e963ac">IDataCollectorCollection</a>



<a href="https://msdn.microsoft.com/e7482bc4-18a4-4267-9ceb-1552dd71391c">IDataCollectorCollection::AddRange</a>



<a href="https://msdn.microsoft.com/7f5a6d20-d65a-477b-8886-8536315bc36e">IDataCollectorCollection::Remove</a>
 

 

