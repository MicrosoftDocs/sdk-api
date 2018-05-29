---
UID: NF:winsync.IAsynchronousDataRetriever.GetIdParameters
title: IAsynchronousDataRetriever::GetIdParameters
author: windows-sdk-content
description: Gets the ID format schema of the provider.
old-location: winsync\iasynchronousdataretriever_getidparameters.htm
old-project: winsync
ms.assetid: 20f42e0d-dacb-4362-843b-8bc2fb664203
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetIdParameters, GetIdParameters method [Windows Sync], GetIdParameters method [Windows Sync],IAsynchronousDataRetriever interface, IAsynchronousDataRetriever interface [Windows Sync],GetIdParameters method, IAsynchronousDataRetriever.GetIdParameters, IAsynchronousDataRetriever::GetIdParameters, winsync.iasynchronousdataretriever_getidparameters, winsync/IAsynchronousDataRetriever::GetIdParameters
ms.prod: windows
ms.technology: windows-sdk
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
-	IAsynchronousDataRetriever.GetIdParameters
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IAsynchronousDataRetriever::GetIdParameters


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




<a href="https://msdn.microsoft.com/38f07582-908b-430e-a886-c0fc24b807ef">IAsynchronousDataRetriever Interface</a>
 

 

