---
UID: NF:ntquery.CITextToFullTree
title: CITextToFullTree function (ntquery.h)
description: Creates a full command tree using Query Language 1.
helpviewer_keywords: ["CITextToFullTree","CITextToFullTree function [Indexing Service]","_idxs_CITextToFullTree","indexsrv.citexttofulltree","ntquery/CITextToFullTree"]
old-location: indexsrv\citexttofulltree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_1mw5.htm
ms.date: 12/05/2018
ms.keywords: CITextToFullTree, CITextToFullTree function [Indexing Service], _idxs_CITextToFullTree, indexsrv.citexttofulltree, ntquery/CITextToFullTree
f1_keywords:
- ntquery/CITextToFullTree
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
- CITextToFullTree
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CITextToFullTree function


## -description


> [!Note]  
> Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use [Windows Search](/windows/desktop/search/-search-3x-wds-overview) for client side search and [Microsoft Search Server Express](https://www.microsoft.com/download/details.aspx?id=18914) for server side search.

Creates a full command tree using Query Language 1.


## -parameters




### -param pwszRestriction

A pointer to a null-terminated string that specifies an Indexing Service query language, Dialect 1 query. 


### -param pwszColumns

A pointer to a null-terminated string that specifies a comma-separated list of column names returned in the query results. These columns can be bound by OLE DB accessors.


### -param pwszSortColumns

A pointer to a null-terminated string that contains a comma separated list of column names that specify the sort order for the query results. A sort direction can be appended to each column name. Use [d] for descending, and [a] for ascending. If no sort order is specified, ascending is the default. This parameter can be <b>NULL</b> for no sort order.


### -param pwszGroupings

A pointer to a null-terminated string that contains a grouping specification made up of a type (currently only [unique] is supported), a property name, and a sort order ([a] for ascending or [d] for descending). In a unique grouping, unique values of the column set form the individual categories. This parameter is optional.

The syntax for the unique grouping term is: 

unique <i>fname</i> [ {[a]|[d]} ] [ , <i>fname2</i> {[a]|[d]} ... ]

where <i>fname</i> and <i>fname2</i> are the assigned friendly names.

Column names separated by a plus sign (+) are grouped in individual categories, and column names following a comma (,) are grouped together into subgroups of the preceding grouping.


### -param ppTree

A pointer to an output variable that receives a pointer to the <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure for the command tree built by the function. 


### -param cProperties

The number of properties in the <i>pProperties</i> array, or <b>NULL</b> if <i>pProperties</i> is zero.


### -param pProperties

A pointer to an array of properties that can be referred to by friendly names in the <i>pwszColumns</i>, <i>pwszSortColumns</i>, <i>pwszGroupings</i>, and <i>pwszRestriction</i> parameters. Column names in the <b>wcsFriendlyName</b> member of each <a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a> structure must be specified in uppercase. This parameter can be <b>NULL</b> if no properties are being defined and <i>cProperties</i> is zero. Indexing Service's built-in properties do not need to be defined to be used. It is an error to define a property with the same friendly name as that of a built-in property.


### -param LocaleID

The locale identifier (LCID) used for nodes in <i>ppTree</i> that contain an LCID member, including such nodes as content restrictions, sort order, and so on. 



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



The query tree allocated by the <b>CITextToFullTree</b> function must be freed either with the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-freecommandtree">ICommandTree::FreeCommandTree</a> method or passed to the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">ICommandTree::SetCommandTree</a> method with the <i>fCopy</i> parameter set to <b>FALSE</b>.



Be sure  to include the following #define directive before your #include &lt;oledberr.h&gt; to access the command tree definitions. 

<pre class="syntax" xml:space="preserve"><code>#define DBINITCONSTANTS
#include &lt;oledberr.h&gt; 
#include &lt;oledb.h&gt; 
#include &lt;cmdtree.h&gt;</code></pre>

#### Examples

This sample code creates a command tree. A custom property from a Microsoft Word document named "IssueNumber" of type "Number" is defined and used in the query. The list of properties returned by the query includes path and size. The sort order is first by rank descending, then by path ascending. The default system locale is used to create the command tree.


```cpp
CIPROPERTYDEF aProperties[1];
const GUID guidOffice = { 0xd5cdd505, 0x2e9c, 0x101b,
                          0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae }
                            };
aProperties[0].wcsFriendlyName = L"ISSUENUMBER";
aProperties[0].dbType = DBTYPE_R8;
aProperties[0].dbCol.uGuid.guid = guidOffice;
aProperties[0].dbCol.eKind = DBKIND_GUID_NAME;
aProperties[0].dbCol.pwszName.ulPropid = L"ISSUENUMBER";
DBCOMMANDTREE * pTree;
HRESULT hr = CiTextToFullTree( L"microsoft and @issuenumber=2",
                               L"size,path,issuenumber",
                               L"rank[d],path[a]",
                               ,
                               &pTree,
                               1,
                               aProperties,
                               GetSystemDefaultLCID() );
if ( SUCCEEDED( hr ) )
{
    hr = pICommandTree->SetCommandTree( pTree,
                                    DBCOMMANDREUSE_NONE,
                                    FALSE );
    if ( SUCCEEDED( hr ) )
    {
        // ...
        // execute a query
        // ...
    }
}

```


The following diagram shows the <i>pTree</i> parameter, created by the example code, of the <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure.

<img alt="" src="./images/dbcmdtr2.png"/>
<div class="code"></div>



## -see-also




<a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>



<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>
 

 