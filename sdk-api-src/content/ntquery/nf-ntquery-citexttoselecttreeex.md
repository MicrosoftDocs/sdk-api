---
UID: NF:ntquery.CITextToSelectTreeEx
title: CITextToSelectTreeEx function (ntquery.h)
description: Creates a SELECT node for a DBCOMMANDTREE structure using the Query Language Dialect that you specify.
helpviewer_keywords: ["CITextToSelectTreeEx","CITextToSelectTreeEx function [Indexing Service]","_idxs_CITextToSelectTreeEx","indexsrv.citexttoselecttreeex","ntquery/CITextToSelectTreeEx"]
old-location: indexsrv\citexttoselecttreeex.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_7jg8.htm
ms.date: 12/05/2018
ms.keywords: CITextToSelectTreeEx, CITextToSelectTreeEx function [Indexing Service], _idxs_CITextToSelectTreeEx, indexsrv.citexttoselecttreeex, ntquery/CITextToSelectTreeEx
f1_keywords:
- ntquery/CITextToSelectTreeEx
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
- CITextToSelectTreeEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CITextToSelectTreeEx function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="/windows/desktop/search/-search-3x-wds-overview">Windows Search</a> for client side search and  <a href=" http://www.microsoft.com/en-us/download/details.aspx?id=18914">Microsoft Search Server Express</a> for server side search.]

Creates a <b>SELECT</b> node for a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure using the Query Language Dialect that you specify.


## -parameters




### -param pwszRestriction

A pointer to a null-terminated string specifying an Indexing Service query. The syntax for queries is described in <a href="/previous-versions/windows/desktop/indexsrv/query-languages-for-indexing-service">Query Languages for Indexing Service</a>. 


### -param ulDialect

A value from <a href="/previous-versions/windows/desktop/indexsrv/isqlang-constants">ISQLANG_*</a> constants that specifies a specific version of the Indexing Service query language to be used.


### -param ppTree

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure for the command tree built by the function. 



### -param cProperties

The number of properties in the <i>pProperties</i> array, or zero if <i>pProperties</i> is <b>NULL</b>.


### -param pProperties

A pointer to an array of properties that can be referred to by friendly name in <i>pwszRestriction</i>. Column names in the <b>wcsFriendlyName</b> member of each <a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a> structure must be specified in uppercase. Indexing Service's built-in properties do not need to be defined to be used. It is an error to define a property with the same friendly name as that of a built-in property.


### -param LocaleID

The locale identifier (LCID) used for nodes in the tree returned in <i>ppTree</i> that contain an LCID member, including such nodes as content restrictions and sort order.


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
The function was denied access to the specified path.

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



Command trees created by the <b>CITextToSelectTreeEx</b> function contain the select portion of a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure. A tree returned by the <b>CITextToSelectTreeEx</b> function can be combined with project and sort nodes to form a complete command tree. Use the <b>CITextToSelectTreeEx</b> function instead of the <a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltreeex">CITextToFullTreeEx</a> function if the sort order and project columns tree nodes are already available.

The query tree allocated by the <b>CITextToSelectTreeEx</b> function must be freed either with the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-freecommandtree">ICommandTree::FreeCommandTree</a> method or passed to the <a href="/previous-versions/windows/desktop/api/cmdtree/nf-cmdtree-icommandtree-setcommandtree">ICommandTree::SetCommandTree</a> method with the <i>fCopy</i> parameter set to <b>FALSE</b>.




#### Examples

This example creates a <a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a> structure. A custom property from a Word document named "IssueNumber" of type "Number" is defined and used in the query.


```cpp
DBCOMMANDTREE * pCompleteTree; 
DBCOMMANDTREE * pTableNode;
 
// ...
// Insert code here to make pCompleteTree a complete tree using pTableNode
// as the DBOP_table_name node that has no query restriction (yet).
// User CoTaskMemAlloc to allocate memory for the nodes.
// ...
//
 
CIPROPERTYDEF aProperties[1];
const GUID guidOffice = { 0xd5cdd505, 0x2e9c, 0x101b,
                          0x93, 0x97, 0x08, 0x00, 0x2b, 0x2c, 0xf9, 0xae }
                         };
aProperties[0].wcsFriendlyName = L"ISSUENUMBER";
aProperties[0].dbType = DBTYPE_R8;
aProperties[0].dbCol.uGuid.guid = guidOffice;
aProperties[0].dbCol.eKind = DBKIND_GUID_NAME;
aProperties[0].dbCol.pwszName.ulPropid = L"ISSUENUMBER";
DBCOMMANDTREE * pSelectTree;
HRESULT hr = CiTextToSelectTreeEx( L"microsoft and @issuenumber=2",
                                 ISQLANG_V1
                                 &pSelectTree,
                                 1,
                                 aProperties,
                                 GetSystemDefaultLCID() );
if ( SUCCEEDED( hr ) )
{
    pTableNode->pctNextSibling = pSelectTree;
    hr = pICommand->SetCommandTree( pCompleteTree,
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





## -see-also




<a href="/windows/desktop/api/ntquery/ns-ntquery-cipropertydef">CIPROPERTYDEF</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-cirestrictiontofulltree">CIRestrictionToFullTree</a>



<a href="/windows/desktop/api/ntquery/nf-ntquery-citexttofulltreeex">CITextToFullTreeEx</a>



<a href="/previous-versions/windows/desktop/indexsrv/dbcommandtree">DBCOMMANDTREE</a>



<a href="/previous-versions/windows/desktop/api/cmdtree/nn-cmdtree-icommandtree">ICommandTree</a>
 

 