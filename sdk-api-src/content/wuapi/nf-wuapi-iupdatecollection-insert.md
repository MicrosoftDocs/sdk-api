---
UID: NF:wuapi.IUpdateCollection.Insert
title: IUpdateCollection::Insert method
author: windows-driver-content
description: Inserts an item into the collection at the specified position.
old-location: wua\iupdatecollection_insert.htm
old-project: Wua_Sdk
ms.assetid: 165f251e-9171-4464-8608-8f365b6598b3
ms.author: windowsdriverdev
ms.date: 3/15/2018
ms.keywords: IUpdateCollection, IUpdateCollection interface [Windows Update Agent], Insert method, IUpdateCollection::Insert, Insert method [Windows Update Agent], Insert method [Windows Update Agent], IUpdateCollection interface, Insert,IUpdateCollection.Insert, wua.iupdatecollection_insert, wuapi/IUpdateCollection::Insert
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: UpdateType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wuapi.dll
api_name:
-	IUpdateCollection.Insert
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateCollection::Insert method


## -description


Inserts an item into the collection at the specified position.


## -parameters




### -param index [in]

The position at which a new interface will be inserted.


### -param value [in]

The <a href="https://msdn.microsoft.com/d0feee2a-96f6-4c86-aaf8-f49d05616fc9">IUpdate</a> interface that will be inserted.


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
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALIDINDEX</b></dt>
</dl>
</td>
<td width="60%">
An index is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e56a09e9-6a5f-4579-9a5c-987519fccaad">IUpdateCollection</a>
 

 

