---
UID: NF:wuapi.IStringCollection.Add
title: IStringCollection::Add (wuapi.h)
author: windows-sdk-content
description: Adds an item to the collection.
old-location: wua\istringcollection_add.htm
tech.root: Wua_Sdk
ms.assetid: f5412e0d-a8b7-43a6-b7a5-95d662459f78
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [Windows Update Agent], Add method [Windows Update Agent],IStringCollection interface, IStringCollection interface [Windows Update Agent],Add method, IStringCollection.Add, IStringCollection::Add, wua.istringcollection_add, wuapi/IStringCollection::Add
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IStringCollection.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStringCollection::Add


## -description


Adds an item to the collection.


## -parameters




### -param value [in]

A string to be added to the collection.


### -param retval [out]

The index of the added interface in the collection.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The collection is read-only.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a>
 

 

