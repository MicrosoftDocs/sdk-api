---
UID: NF:sensorsapi.ISensorCollection.GetCount
title: ISensorCollection::GetCount
author: windows-sdk-content
description: Retrieves the count of sensors in the collection.
old-location: winsensors_com_ref\isensorcollection_getcount.htm
old-project: SensorsAPI
ms.assetid: 40bcf993-55fb-4d75-91dc-44d770a0e226
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCount, GetCount method, GetCount method,ISensorCollection interface, ISensorCollection interface,GetCount method, ISensorCollection.GetCount, ISensorCollection::GetCount, sensorsapi/ISensorCollection::GetCount, winsensors_com_ref.isensorcollection_getcount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: sensorsapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SensorConnectionType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sensorsapi.dll
api_name:
 - ISensorCollection.GetCount
product: Windows
targetos: Windows
req.lib: Sensorsapi.lib
req.dll: Sensorsapi.dll
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/54d8572a-40a2-49d0-a8bf-2161b63eee42">ISensorCollection</a>
 

 

