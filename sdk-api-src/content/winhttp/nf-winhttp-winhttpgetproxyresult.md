---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# WinHttpGetProxyResult function


## -description


The <b>WinHttpGetProxyResult</b> function retrieves the results of a call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


## -parameters




### -param hResolver [in]

The resolver handle used to issue a previously completed call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.


### -param pProxyResult [out]

A pointer to a <a href="https://msdn.microsoft.com/6a621701-3325-4877-99ba-8580ad07739d">WINHTTP_PROXY_RESULT</a> structure that contains the results of a previous call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.  The results must be freed by calling <a href="https://msdn.microsoft.com/0484bf54-066f-4a7f-8d1a-079eb4b001bd">WinHttpFreeProxyResult</a>.


## -returns



A status code indicating the result of the operation.

<table>
<tr>
<th>The following codes may be returned.</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The type of handle supplied is incorrect for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WINHTTP_INCORRECT_HANDLE_STATE</b></dt>
</dl>
</td>
<td width="60%">
The resolver handle has not successfully completed a call to <a href="https://msdn.microsoft.com/28479a55-7a25-4254-b27a-45e09b166dd5">WinHttpGetProxyForUrlEx</a>.

</td>
</tr>
</table>
 



