---
UID: NF:searchapi.ISearchQueryHelper.get_ConnectionString
title: ISearchQueryHelper::get_ConnectionString
author: windows-sdk-content
description: Returns the OLE DB connection string for the Window Search index.
old-location: search\_search_ISearchQueryHelper_get_ConnectionString.htm
old-project: search
ms.assetid: VS|search|~\search\wds3x\reference\ifaces\querying\isearchqueryhelper\get_connectionstring.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISearchQueryHelper interface [search],get_ConnectionString method, ISearchQueryHelper.get_ConnectionString, ISearchQueryHelper::get_ConnectionString, _search_ISearchQueryHelper_get_ConnectionString, get_ConnectionString, get_ConnectionString method [search], get_ConnectionString method [search],ISearchQueryHelper interface, search._search_ISearchQueryHelper_get_ConnectionString, searchapi/ISearchQueryHelper::get_ConnectionString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: searchapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Searchquery.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: ROWSETEVENT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Searchapi.h
api_name:
 - ISearchQueryHelper.get_ConnectionString
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ISearchQueryHelper::get_ConnectionString


## -description


Returns the OLE DB connection string for the Window Search index.


## -parameters




### -param pszConnectionString






#### - pwszConnectionString [out, retval]

Type: <b>LPWSTR*</b>

Receives a pointer to a null-terminated Unicode string that is a valid OLE DB connection string. This connection string can be used to initialize a connection to the Windows Search index and submit the SQL query returned by  <a href="https://msdn.microsoft.com/846c0c05-c227-487c-8512-7644b80db8d8">ISearchQueryHelper::GenerateSQLFromUserQuery</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A connection string is a string version of the initialization properties needed to connect to a data store. The string can include such things as a data source, data source name, or user ID and password.

The DSearch code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates how to create a class for a static console application to query Windows Search using the Microsoft.Search.Interop assembly for <a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>.




## -see-also




<a href="https://msdn.microsoft.com/1e075961-63b7-4d91-b6ea-5d06d5b81140">ISearchQueryHelper</a>



<a href="https://msdn.microsoft.com/2c161b7f-4e28-4e8a-add6-3c1cda00a622">Querying the Index Programmatically</a>



<a href="https://msdn.microsoft.com/a2eb550a-bb55-4dbd-9ca1-60b776eb9339">Querying the Index with Windows Search SQL Syntax</a>
 

 

