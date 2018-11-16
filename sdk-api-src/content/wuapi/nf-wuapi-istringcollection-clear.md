---
UID: NF:wuapi.IStringCollection.Clear
title: IStringCollection::Clear
author: windows-sdk-content
description: Removes all the elements from the collection.
old-location: wua\istringcollection_clear.htm
tech.root: Wua_Sdk
ms.assetid: 480b8a8a-ecf1-4f1c-b53d-98a0151c57b5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Clear, Clear method [Windows Update Agent], Clear method [Windows Update Agent],IStringCollection interface, IStringCollection interface [Windows Update Agent],Clear method, IStringCollection.Clear, IStringCollection::Clear, wua.istringcollection_clear, wuapi/IStringCollection::Clear
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
 - IStringCollection.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wuapi.h
: 
- IStringCollection.Clear
: 
---

# IStringCollection::Clear


## -description


Removes all the elements from the collection.


## -parameters






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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a>
 

 

