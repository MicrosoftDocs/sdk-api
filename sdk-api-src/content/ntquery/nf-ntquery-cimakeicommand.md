---
UID: NF:ntquery.CIMakeICommand
title: CIMakeICommand function (ntquery.h)
description: Creates a Command object, specifying computers, catalogs, and scopes.
helpviewer_keywords: ["CIMakeICommand","CIMakeICommand function [Indexing Service]","_idxs_CIMakeICommand","indexsrv.cimakeicommand","ntquery/CIMakeICommand"]
old-location: indexsrv\cimakeicommand.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_9u90.htm
ms.date: 12/05/2018
ms.keywords: CIMakeICommand, CIMakeICommand function [Indexing Service], _idxs_CIMakeICommand, indexsrv.cimakeicommand, ntquery/CIMakeICommand
f1_keywords:
- ntquery/CIMakeICommand
dev_langs:
- c++
req.header: ntquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Ntquery.dll
api_name:
- CIMakeICommand
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CIMakeICommand function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Creates a Command object, specifying computers, catalogs, and scopes.


## -parameters




### -param ppCommand

A pointer to an output variable that receives the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface pointer.


### -param cScope

The number of scopes in the <i>awcsScope</i> array.


### -param aDepths

A pointer to an array of values that represent the type of search (deep or shallow, virtual or physical) for each scope in <i>awcsScope</i>. For the possible values for each scope, see <a href="/previous-versions/windows/desktop/indexsrv/query-scope-constants">QUERY_*</a> scope constants.


### -param awcsScope

A pointer to a an array of null-terminated strings that specify the names of the file path(s) over which the query is processed. This is the value for the DBPROP_CI_INCLUDE_SCOPE property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface. Use L"\" for the entire catalog. Use L"\" for the entire Internet Information Services (IIS) virtual-path namespace, but set QUERY_VIRTUAL_PATH in the <i>aDepths</i> parameter to indicate that the path is virtual.


### -param awcsCatalogs

A pointer to a an array of null-terminated strings that specify the names of the catalogs used to execute queries. This is the value for the DBPROP_CI_CATALOG_NAME property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface. 


### -param awcsMachine

A pointer to a null-terminated string that specifies the name of the computer on which the query is to be executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface. Use L"." for the local computer.


## -returns



This function can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The function was denied access to a specified path.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The function encountered an invalid handle, probably due to a low-memory situation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The function received an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function did not have sufficient memory or other resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unknown error has occurred.

</td>
</tr>
</table>
 




## -remarks



The <b>CIMakeICommand</b> function does not return an error if the catalog or computer does not exist or is unavailable. The connection to the catalog and computer is established when the <b>ICommand::Execute</b> method is called, and connection errors are returned at that time.




## -see-also




<a href="/windows/desktop/api/ntquery/nf-ntquery-cicreatecommand">CICreateCommand</a>



<a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a>
 

 