---
UID: NF:wuapi.IStringCollection.RemoveAt
title: IStringCollection::RemoveAt
author: windows-sdk-content
description: Removes the item at the specified index from the collection.
old-location: wua\istringcollection_removeat.htm
old-project: Wua_Sdk
ms.assetid: a0b350b0-d5b4-49c6-acca-a50719d92262
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IStringCollection interface [Windows Update Agent],RemoveAt method, IStringCollection.RemoveAt, IStringCollection::RemoveAt, RemoveAt, RemoveAt method [Windows Update Agent], RemoveAt method [Windows Update Agent],IStringCollection interface, wua.istringcollection_removeat, wuapi/IStringCollection::RemoveAt
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UpdateType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IStringCollection.RemoveAt
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IStringCollection::RemoveAt


## -description


Removes the item at the specified index from the collection.


## -parameters




### -param index [in]

The index of the string to be removed.


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




<a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a>
 

 

