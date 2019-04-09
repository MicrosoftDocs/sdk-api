---
UID: NF:ntquery.CICreateCommand
title: CICreateCommand function (ntquery.h)
author: windows-sdk-content
description: Creates a Command object.
old-location: indexsrv\cicreatecommand.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_3sys.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CICreateCommand, CICreateCommand function [Indexing Service], _idxs_CICreateCommand, indexsrv.cicreatecommand, ntquery/CICreateCommand
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CICreateCommand function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href="http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Creates a Command object.


## -parameters




### -param ppCommand

A pointer to a variable that receives the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer requested in <i>riid</i>.


### -param pUnkOuter

A pointer to an optional outer <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. This parameter can be zero for no aggregation, in which case <i>riid</i> can contain a value other than IID_IUnknown.


### -param riid

The interface identifier (IID) of the interface returned in <i>ppCommand</i>. This parameter must be IID_IUnknown unless <i>pUnkOuter</i> is <b>NULL</b>. Pass IID_ICommand to get an <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface if aggregation isn't needed and <i>pUnkOuter</i> is <b>NULL</b>.


### -param pwcsCatalog

The name of the catalog to be used to execute queries. This is the value for the DBPROP_CI_CATALOG_NAME property of the <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface.


### -param pwcsMachine

The name of the computer on which the query is to be executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface. Use L"." for the local computer.


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



The <b>CICreateCommand</b> function simplifies the task of connecting to the Indexing Service content and property indexes as an OLE DB provider data source object (DSO) and creating a session object. Queries made with the resulting <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface default to the scope "\" and search everywhere under that hierarchy (a "deep" search). To specify a scope, use <a href="https://msdn.microsoft.com/en-us/library/ms691127(v=VS.85).aspx">CIMakeICommand</a>.

If interface aggregation isn't required, pass IID_ICommand for riid and <b>NULL</b> for <i>pUnkOuter</i>. Otherwise, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on the returned object to get an <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface.

The <b>CICreateCommand</b> function does not return an error if the catalog or computer do not exist or are not available. The connection to the catalog and computer are established when the <b>ICommand::Execute</b> method is called, and connection errors are returned at that time.



Additional catalog, computer, and scope parameters can be specified after an <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface is created using the <a href="https://msdn.microsoft.com/library/ms723044(v=VS.85).aspx">ICommandProperties</a> interface.

A pointer to a null-terminated string that specifies the name of the machine on which the query is executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface. Use L"." for the local computer.


#### Examples

This example creates an <a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a> interface for the system catalog on the local machine.


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




<a href="https://msdn.microsoft.com/en-us/library/ms691127(v=VS.85).aspx">CIMakeICommand</a>



<a href="https://msdn.microsoft.com/library/ms709737(v=VS.85).aspx">ICommand</a>



<a href="https://msdn.microsoft.com/library/ms723044(v=VS.85).aspx">ICommandProperties</a>
 

 

