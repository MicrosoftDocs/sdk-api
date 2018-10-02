---
UID: NF:wuapi.IStringCollection.Copy
title: IStringCollection::Copy
author: windows-sdk-content
description: Creates a deep read/write copy of the collection.
old-location: wua\istringcollection_copy.htm
tech.root: Wua_Sdk
ms.assetid: e2f6d5c0-c92a-44e5-a322-f336a3ef64ce
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Copy, Copy method [Windows Update Agent], Copy method [Windows Update Agent],IStringCollection interface, IStringCollection interface [Windows Update Agent],Copy method, IStringCollection.Copy, IStringCollection::Copy, wua.istringcollection_copy, wuapi/IStringCollection::Copy
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
 - IStringCollection.Copy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStringCollection::Copy


## -description


Creates a deep read/write copy of the collection.


## -parameters




### -param retval [out]

A deep read/write copy of the collection.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a>
 

 

