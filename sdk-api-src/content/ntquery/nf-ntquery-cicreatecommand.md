---
UID: NF:ntquery.CICreateCommand
title: CICreateCommand function
author: windows-sdk-content
description: Creates a Command object.
old-location: indexsrv\cicreatecommand.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_3sys.htm
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CICreateCommand, CICreateCommand function [Indexing Service], _idxs_CICreateCommand, indexsrv.cicreatecommand, ntquery/CICreateCommand
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MediaLabelInfo, *pMediaLabelInfo
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
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
req.product: ADAM
---

# CICreateCommand function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Creates a Command object.


## -parameters




### -param ppCommand

A pointer to a variable that receives the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface pointer requested in <i>riid</i>.


### -param pUnkOuter

A pointer to an optional outer <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. This parameter can be zero for no aggregation, in which case <i>riid</i> can contain a value other than IID_IUnknown.


### -param riid

The interface identifier (IID) of the interface returned in <i>ppCommand</i>. This parameter must be IID_IUnknown unless <i>pUnkOuter</i> is <b>NULL</b>. Pass IID_ICommand to get an <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface if aggregation isn't needed and <i>pUnkOuter</i> is <b>NULL</b>.


### -param pwcsCatalog

The name of the catalog to be used to execute queries. This is the value for the DBPROP_CI_CATALOG_NAME property of the <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface.


### -param pwcsMachine

The name of the computer on which the query is to be executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface. Use L"." for the local computer.


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



The <b>CICreateCommand</b> function simplifies the task of connecting to the Indexing Service content and property indexes as an OLE DB provider data source object (DSO) and creating a session object. Queries made with the resulting <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface default to the scope "\" and search everywhere under that hierarchy (a "deep" search). To specify a scope, use <a href="https://msdn.microsoft.com/e5586d00-996f-4a0f-a283-03d18a516115">CIMakeICommand</a>.

If interface aggregation isn't required, pass IID_ICommand for riid and <b>NULL</b> for <i>pUnkOuter</i>. Otherwise, call <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> on the returned object to get an <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface.

The <b>CICreateCommand</b> function does not return an error if the catalog or computer do not exist or are not available. The connection to the catalog and computer are established when the <b>ICommand::Execute</b> method is called, and connection errors are returned at that time.



Additional catalog, computer, and scope parameters can be specified after an <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface is created using the <a href="cfda4b13-b99f-4b66-ad2b-bd9584c8b3ef">ICommandProperties</a> interface.

A pointer to a null-terminated string that specifies the name of the machine on which the query is executed. This is the value for the DBPROP_CI_MACHINE_NAME property of the <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface. Use L"." for the local computer.


#### Examples

This example creates an <a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a> interface for the system catalog on the local machine.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>ICommand * pICommand;
HRESULT hr = CICreateCommand( (IUnknown **) &amp;pICommand, 0, IID_ICommand, L"system", L"." );
if ( SUCCEEDED( hr ) )
{
    // ...
    // execute one or more queries with the ICommand
    // ...
    pICommand-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/e5586d00-996f-4a0f-a283-03d18a516115">CIMakeICommand</a>



<a href="089427ad-5ba3-4613-b89e-8e86420ccc30">ICommand</a>



<a href="cfda4b13-b99f-4b66-ad2b-bd9584c8b3ef">ICommandProperties</a>
 

 

