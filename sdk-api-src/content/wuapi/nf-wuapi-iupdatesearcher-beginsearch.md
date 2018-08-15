---
UID: NF:wuapi.IUpdateSearcher.BeginSearch
title: IUpdateSearcher::BeginSearch
author: windows-sdk-content
description: Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.
old-location: wua\iupdatesearcherbeginsearch.htm
old-project: wua_sdk
ms.assetid: 8af818b1-7dd8-4f48-b447-5b6dfbfce420
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: BeginSearch, BeginSearch method [Windows Update Agent], BeginSearch method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],BeginSearch method, IUpdateSearcher.BeginSearch, IUpdateSearcher::BeginSearch, wua.iupdatesearcherbeginsearch, wuapi/IUpdateSearcher::BeginSearch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.redist: 
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
 - IUpdateSearcher.BeginSearch
product: Windows
targetos: Windows
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IUpdateSearcher::BeginSearch


## -description


Begins execution of an asynchronous search for updates. The search uses the search options that are currently configured.


## -parameters




### -param criteria [in]

A string that specifies the search criteria.


### -param onCompleted [in]

An <a href="https://msdn.microsoft.com/f228808d-7f7e-4107-a4b6-4bac5b48d1b4">ISearchCompletedCallback</a> interface that is called when an asynchronous search operation is complete.


### -param state [in]

The caller-specific  state that is returned by the <a href="https://msdn.microsoft.com/68d861a3-420d-4a89-ac32-900db6d51036">AsyncState</a> property of the <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface.


### -param retval [out]

An <a href="https://msdn.microsoft.com/aec4a812-cf5d-4986-a776-29c366bb1771">ISearchJob</a> interface that represents the current operation that might be pending. 

The caller passes the returned value to the <a href="https://msdn.microsoft.com/4a0532ec-3613-4aa1-96d7-7291b9ca7a94">EndSearch</a> method to complete a search operation.


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
 




## -remarks



For a complete description of search criteria syntax, see <a href="https://msdn.microsoft.com/0511cfd0-f4de-41ab-af35-32d757217386">Search</a>.

  As an alternative to implementing the <a href="https://msdn.microsoft.com/f228808d-7f7e-4107-a4b6-4bac5b48d1b4">ISearchCompletedCallback</a> interface, you can use a script to   implement a callback routine of any identifier with DISPID 0 on an automation object. The type of the <i>onCompleted</i> parameter is <b>IUnknown*</b>.

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="https://msdn.microsoft.com/1fb16904-732d-4341-8267-ab8896fc0f7c">Guidelines for Asynchronous WUA Operations</a>.





## -see-also




<a href="https://msdn.microsoft.com/f41b1689-d9fe-4697-91e9-a176d3b592c7">IUpdateSearcher</a>
 

 

