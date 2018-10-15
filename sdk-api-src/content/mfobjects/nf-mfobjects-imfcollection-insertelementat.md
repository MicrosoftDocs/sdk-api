---
UID: NF:mfobjects.IMFCollection.InsertElementAt
title: IMFCollection::InsertElementAt
author: windows-sdk-content
description: Adds an object at the specified index in the collection.
old-location: mf\imfcollection_insertelementat.htm
tech.root: medfound
ms.assetid: d8f64bf8-eb5b-4673-91be-796f4ea8dce0
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMFCollection interface [Media Foundation],InsertElementAt method, IMFCollection.InsertElementAt, IMFCollection::InsertElementAt, InsertElementAt, InsertElementAt method [Media Foundation], InsertElementAt method [Media Foundation],IMFCollection interface, d8f64bf8-eb5b-4673-91be-796f4ea8dce0, mf.imfcollection_insertelementat, mfobjects/IMFCollection::InsertElementAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFCollection.InsertElementAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCollection::InsertElementAt


## -description



Adds an object at the specified index in the collection.




## -parameters




### -param dwIndex [in]

The zero-based index where the object will be added to the collection.


### -param pUnknown [in]

The object to insert.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a>
 

 

