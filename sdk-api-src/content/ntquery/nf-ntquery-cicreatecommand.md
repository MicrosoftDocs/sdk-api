---
UID: NF:ntquery.CICreateCommand
title: CICreateCommand function (ntquery.h)
description: Creates a Command object.
helpviewer_keywords: ["CICreateCommand","CICreateCommand function [Indexing Service]","_idxs_CICreateCommand","indexsrv.cicreatecommand","ntquery/CICreateCommand"]
old-location: indexsrv\cicreatecommand.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_3sys.htm
ms.date: 12/05/2018
ms.keywords: CICreateCommand, CICreateCommand function [Indexing Service], _idxs_CICreateCommand, indexsrv.cicreatecommand, ntquery/CICreateCommand
f1_keywords:
- ntquery/CICreateCommand
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
- CICreateCommand
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CICreateCommand function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Creates a Command object.


## -parameters




### -param ppCommand

A pointer to a variable that receives the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer requested in <i>riid</i>.


### -param pUnkOuter

A pointer to an optional outer <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. This parameter can be zero for no aggregation, in which case <i>riid</i> can contain a value other than IID_IUnknown.


### -param riid

The interface identifier (IID) of the interface returned in <i>ppCommand</i>. This parameter must be IID_IUnknown unless <i>pUnkOuter</i> is <b>NULL</b>. Pass IID_ICommand to get an <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface if aggregation isn't needed and <i>pUnkOuter</i> is <b>NULL</b>.


### -param pwcsCatalog

The name of the catalog to be used to execute queries. This is the value for the DBPROP_CI_CATALOG_NAME property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface.


### -param pwcsMachine

The name of the computer on which the query is to be executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface. Use L"." for the local computer.


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
<dt><b>CLASS_E_NOAGGREGATION</b></dt>
</dl>
</td>
<td width="60%">
Aggregation exists (<i>pUnkOuter</i> is not <b>NULL</b>) and <i>riid</i> is not IID_IUnknown.

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
</table>
 




## -remarks



The <b>CICreateCommand</b> function simplifies the task of connecting to the Indexing Service content and property indexes as an OLE DB provider data source object (DSO) and creating a session object. Queries made with the resulting <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface default to the scope "\" and search everywhere under that hierarchy (a "deep" search). To specify a scope, use <a href="/windows/desktop/api/ntquery/nf-ntquery-cimakeicommand">CIMakeICommand</a>.

If interface aggregation isn't required, pass IID_ICommand for riid and <b>NULL</b> for <i>pUnkOuter</i>. Otherwise, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> on the returned object to get an <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface.

The <b>CICreateCommand</b> function does not return an error if the catalog or computer do not exist or are not available. The connection to the catalog and computer are established when the <b>ICommand::Execute</b> method is called, and connection errors are returned at that time.



Additional catalog, computer, and scope parameters can be specified after an <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface is created using the <a href="/previous-versions/windows/desktop/ms723044(v=vs.85)">ICommandProperties</a> interface.

A pointer to a null-terminated string that specifies the name of the machine on which the query is executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface. Use L"." for the local computer.


#### Examples

This example creates an <a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a> interface for the system catalog on the local machine.


```
ICommand * pICommand;
HRESULT hr = CICreateCommand( (IUnknown **) &pICommand, 0, IID_ICommand, L"system", L"." );
if ( SUCCEEDED( hr ) )
{
    // ...
    // execute one or more queries with the ICommand
    // ...
    pICommand->Release();
}

```





## -see-also




<a href="/windows/desktop/api/ntquery/nf-ntquery-cimakeicommand">CIMakeICommand</a>



<a href="/previous-versions/windows/desktop/ms709737(v=vs.85)">ICommand</a>



<a href="/previous-versions/windows/desktop/ms723044(v=vs.85)">ICommandProperties</a>
 

 