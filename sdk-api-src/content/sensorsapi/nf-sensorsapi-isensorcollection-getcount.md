---
UID: NF:sensorsapi.ISensorCollection.GetCount
title: ISensorCollection::GetCount (sensorsapi.h)
description: Retrieves the count of sensors in the collection.
old-location: winsensors_com_ref\isensorcollection_getcount.htm
tech.root: SensorsAPI
ms.assetid: 40bcf993-55fb-4d75-91dc-44d770a0e226
ms.date: 12/05/2018
ms.keywords: GetCount, GetCount method, GetCount method,ISensorCollection interface, ISensorCollection interface,GetCount method, ISensorCollection.GetCount, ISensorCollection::GetCount, sensorsapi/ISensorCollection::GetCount, winsensors_com_ref.isensorcollection_getcount
f1_keywords:
- sensorsapi/ISensorCollection.GetCount
dev_langs:
- c++
req.header: sensorsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- sensorsapi.dll
api_name:
- ISensorCollection.GetCount
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISensorCollection::GetCount


## -description


Retrieves the count of sensors in the collection.


## -parameters




### -param pCount [out]

Address of a <b>ULONG</b> that receives the count.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL was passed in for pCount.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorcollection">ISensorCollection</a>
 

 

