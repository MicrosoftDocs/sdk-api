---
UID: NF:winsync.ISynchronousDataRetriever.GetIdParameters
title: ISynchronousDataRetriever::GetIdParameters
author: windows-driver-content
description: Gets the ID format schema of the provider.
old-location: winsync\isynchronousdataretriever_getidparameters.htm
old-project: winsync
ms.assetid: 98273eec-93fd-44ae-a1c9-cf85790dfc1d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],ISynchronousDataRetriever interface, ISynchronousDataRetriever interface [Windows Sync],GetIdParameters method, ISynchronousDataRetriever.GetIdParameters, ISynchronousDataRetriever::GetIdParameters, winsync.isynchronousdataretriever_getidparameters, winsync/ISynchronousDataRetriever::GetIdParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: winsync.h
req.include-header: 
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISynchronousDataRetriever.GetIdParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISynchronousDataRetriever::GetIdParameters


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
 




## -see-also




<a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever Interface</a>
 

 

