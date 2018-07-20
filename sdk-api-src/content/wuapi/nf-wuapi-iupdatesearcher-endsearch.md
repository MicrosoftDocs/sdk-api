---
UID: NF:wuapi.IUpdateSearcher.EndSearch
title: IUpdateSearcher::EndSearch
author: windows-sdk-content
description: Completes an asynchronous search for updates.
old-location: wua\iupdatesearcherendsearch.htm
old-project: Wua_Sdk
ms.assetid: 4a0532ec-3613-4aa1-96d7-7291b9ca7a94
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: EndSearch, EndSearch method [Windows Update Agent], EndSearch method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],EndSearch method, IUpdateSearcher.EndSearch, IUpdateSearcher::EndSearch, wua.iupdatesearcherendsearch, wuapi/IUpdateSearcher::EndSearch
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
 - IUpdateSearcher.EndSearch
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSearcher::EndSearch


## -description


Completes an asynchronous search for updates.


## -parameters




### -param searchJob [in]

The <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface that the <a href="https://msdn.microsoft.com/8af818b1-7dd8-4f48-b447-5b6dfbfce420">BeginSearch</a> method returns.


### -param retval [out]

An <a href="https://msdn.microsoft.com/f38c5b0f-8010-4db1-802c-5005c332188b">ISearchResult</a> interface that contains the following:

<ul>
<li>The result of an operation</li>
<li>A collection of updates that match the search criteria</li>
</ul>

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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
An  asynchronous search for updates is  successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_LEGACYSERVER</b></dt>
</dl>
</td>
<td width="60%">
You cannot search for updates if the <a href="https://msdn.microsoft.com/b514545a-d983-491b-9a28-540bd5c4c128">ServerSelection</a> property of <a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a> is set to <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ssManagedServer</a> or to <a href="https://msdn.microsoft.com/51caac5e-98a6-49e4-a175-6319349a6d68">ssDefault</a>, and the managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/4a0532ec-3613-4aa1-96d7-7291b9ca7a94">EndSearch</a> method returns <b>WU_E_INVALID_OPERATION</b> if <b>EndSearch</b> has already been called for the search  job.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_CRITERIA</b></dt>
</dl>
</td>
<td width="60%">
An invalid criteria was encountered during a search.

</td>
</tr>
</table>
 




## -remarks



When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

