---
UID: NF:pla.IDataCollectorCollection.Add
title: IDataCollectorCollection::Add (pla.h)
author: windows-sdk-content
description: Adds a data collector to the collection.
old-location: pla\idatacollectorcollection_add.htm
tech.root: PLA
ms.assetid: 6302e144-74ef-4251-a857-d3e066c9763d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [PLA], Add method [PLA],IDataCollectorCollection interface, IDataCollectorCollection interface [PLA],Add method, IDataCollectorCollection.Add, IDataCollectorCollection::Add, base.idatacollectorcollection_add, pla.idatacollectorcollection_add, pla/IDataCollectorCollection::Add
ms.topic: method
f1_keywords: 
 - "pla/IDataCollectorCollection.Add"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorCollection::Add


## -description


Adds a data collector to the collection.


## -parameters




### -param collector [in]

An <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> interface of the data collector to add to this collection.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollectorcollection">IDataCollectorCollection</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-addrange">IDataCollectorCollection::AddRange</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-remove">IDataCollectorCollection::Remove</a>
 

 

