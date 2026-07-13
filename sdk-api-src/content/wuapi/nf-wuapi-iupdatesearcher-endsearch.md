---
UID: NF:wuapi.IUpdateSearcher.EndSearch
title: IUpdateSearcher::EndSearch (wuapi.h)
description: Completes an asynchronous search for updates.
helpviewer_keywords: ["EndSearch","EndSearch method [Windows Update Agent]","EndSearch method [Windows Update Agent]","IUpdateSearcher interface","IUpdateSearcher interface [Windows Update Agent]","EndSearch method","IUpdateSearcher.EndSearch","IUpdateSearcher::EndSearch","wua.iupdatesearcherendsearch","wuapi/IUpdateSearcher::EndSearch"]
old-location: wua\iupdatesearcherendsearch.htm
tech.root: wua
ms.assetid: 4a0532ec-3613-4aa1-96d7-7291b9ca7a94
ms.date: 12/05/2018
ms.keywords: EndSearch, EndSearch method [Windows Update Agent], EndSearch method [Windows Update Agent],IUpdateSearcher interface, IUpdateSearcher interface [Windows Update Agent],EndSearch method, IUpdateSearcher.EndSearch, IUpdateSearcher::EndSearch, wua.iupdatesearcherendsearch, wuapi/IUpdateSearcher::EndSearch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateSearcher::EndSearch
 - wuapi/IUpdateSearcher::EndSearch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateSearcher.EndSearch
---

# IUpdateSearcher::EndSearch


## -description

Completes an asynchronous search for updates.

## -parameters

### -param searchJob [in]

The <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchjob">ISearchJob</a> interface that the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-beginsearch">BeginSearch</a> method returns.

### -param retval [out]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-isearchresult">ISearchResult</a> interface that contains the following:

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
<dt><b>S_OK</b></dt>
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
You cannot search for updates if the <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-get_serverselection">ServerSelection</a> property of <a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a> is set to <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssManagedServer</a> or to <a href="https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/wuapicommon/ne-wuapicommon-serverselection.md">ssDefault</a>, and the managed server on a computer is a Microsoft Software Update Services (SUS) 1.0 server.

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
The <a href="/windows/desktop/api/wuapi/nf-wuapi-iupdatesearcher-endsearch">EndSearch</a> method returns <b>WU_E_INVALID_OPERATION</b> if <b>EndSearch</b> has already been called for the search  job.

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

When you use any asynchronous WUA API in your app, you might need to implement a time-out mechanism. For more info about how to perform asynchronous WUA operations, see <a href="/windows/desktop/Wua_Sdk/guidelines-for-asynchronous-wua-operations">Guidelines for Asynchronous WUA Operations</a>.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdatesearcher">IUpdateSearcher</a>