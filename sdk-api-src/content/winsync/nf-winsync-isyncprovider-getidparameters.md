---
UID: NF:winsync.ISyncProvider.GetIdParameters
title: ISyncProvider::GetIdParameters
author: windows-sdk-content
description: Gets the ID format schema of the provider.
old-location: winsync\isyncprovider_getidparameters.htm
old-project: winsync
ms.assetid: a1839c53-7978-4a14-8b17-43621b801f13
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],ISyncProvider interface, ISyncProvider interface [Windows Sync],GetIdParameters method, ISyncProvider.GetIdParameters, ISyncProvider::GetIdParameters, winsync.isyncprovider_getidparameters, winsync/ISyncProvider::GetIdParameters
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: winsync.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISyncProvider.GetIdParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncProvider::GetIdParameters


## -description


Gets the ID format schema of the provider.


## -parameters




### -param pIdParameters [out]

Returns the ID format schema of the provider.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



This method is used to get the ID format schema from the two providers that are participating in synchronization. A synchronization session should use this method to verify that the two providers have the same ID format schema, so that they can synchronize with one another.




## -see-also




<a href="https://msdn.microsoft.com/7391689a-5546-409a-9fff-2ceced1850fe">ID_PARAMETERS Structure</a>



<a href="https://msdn.microsoft.com/0664267f-90ba-4123-bfe5-7cf748b78c10">ISyncProvider Interface</a>
 

 

