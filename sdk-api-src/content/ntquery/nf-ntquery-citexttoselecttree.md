---
UID: NF:ntquery.CITextToSelectTree
title: CITextToSelectTree function
author: windows-sdk-content
description: Creates a SELECT node for a DBCOMMANDTREE structure using Query Language Dialect 1.
old-location: indexsrv\citexttoselecttree.htm
tech.root: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_1t0l.htm
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: CITextToSelectTree, CITextToSelectTree function [Indexing Service], _idxs_CITextToSelectTree, indexsrv.citexttoselecttree, ntquery/CITextToSelectTree
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CITextToSelectTree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CITextToSelectTree function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/en-us/library/Aa965362(v=VS.85).aspx">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Creates a <b>SELECT</b> node for a <a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a> structure using Query Language Dialect 1.


## -parameters




### -param pwszRestriction

A pointer to a null-terminated string specifying an Indexing Service Query Language Dialect 1 query.


### -param ppTree

A pointer to the address of the location to receive the <a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a> structure that represents the top node of the <b>SELECT</b> part of the full command tree.


### -param cProperties

The number of properties in the <i>pProperties</i> array, or zero if <i>pProperties</i> is <b>NULL</b>.


### -param pProperties

A pointer to an array of properties that can be referred to by friendly name in <i>pwszRestriction</i>. Column names in the <b>wcsFriendlyName</b> member of each <a href="https://msdn.microsoft.com/en-us/library/ms690848(v=VS.85).aspx">CIPROPERTYDEF</a> structure must be specified in uppercase. Indexing Service's built-in properties do not need to be defined to be used. It is an error to define a property with the same friendly name as that of a built-in property.


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



Command trees created by <b>CITextToSelectTree</b> contain the <b>SELECT</b> portion of a <a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a> structure. A tree returned by <b>CITextToSelectTree</b> can be combined with project and sort nodes to form a complete command tree. Use <b>CITextToSelectTree</b> instead of the <a href="https://msdn.microsoft.com/en-us/library/ms690933(v=VS.85).aspx">CITextToFullTree</a> function if the sort order and project columns tree nodes are already available.

The query tree allocated by <b>CITextToSelectTree</b> must be freed either with the <a href="https://msdn.microsoft.com/en-us/library/ms689884(v=VS.85).aspx">ICommandTree::FreeCommandTree</a> method or passed to the <a href="https://msdn.microsoft.com/en-us/library/ms690251(v=VS.85).aspx">ICommandTree::SetCommandTree</a> method with the <i>fCopy</i> parameter set to <b>FALSE</b>.


#### Examples

This example creates a <a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a> structure. A custom property from a Word document named "IssueNumber" of type "Number" is defined and used in the query.




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
HRESULT hr = CiTextToSelectTree( L"Microsoft and @issuenumber=2",
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


The following diagram shows the <a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a> structure pSelectTree created by the example code.



<img alt="" src="./images/dbcmdtr1.png"/>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690848(v=VS.85).aspx">CIPROPERTYDEF</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690954(v=VS.85).aspx">CIRestrictionToFullTree</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691026(v=VS.85).aspx">CITextToSelectTreeEx</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689889(v=VS.85).aspx">DBCOMMANDTREE</a>



<a href="https://msdn.microsoft.com/en-us/library/ms689746(v=VS.85).aspx">ICommandTree</a>
 

 

