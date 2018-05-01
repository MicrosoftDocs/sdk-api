---
UID: NF:wuapi.IUpdateCollection.Copy
title: IUpdateCollection::Copy method
author: windows-driver-content
description: Creates a shallow read/write copy of the collection.
old-location: wua\iupdatecollection_copy.htm
old-project: Wua_Sdk
ms.assetid: 78a024a4-7aab-4bcb-bd3f-a79ef5580e1b
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: Copy method [Windows Update Agent], Copy method [Windows Update Agent], IUpdateCollection interface, Copy,IUpdateCollection.Copy, IUpdateCollection, IUpdateCollection interface [Windows Update Agent], Copy method, IUpdateCollection::Copy, wua.iupdatecollection_copy, wuapi/IUpdateCollection::Copy
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
-	IUpdateCollection.Copy
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateCollection::Copy method


## -description


Creates a shallow read/write copy of the collection.


## -parameters




### -param retval [out]

A shallow read/write copy of the collection.


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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e56a09e9-6a5f-4579-9a5c-987519fccaad">IUpdateCollection</a>
 

 

