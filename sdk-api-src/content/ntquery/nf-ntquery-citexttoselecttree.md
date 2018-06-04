---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CITextToSelectTree function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Creates a <b>SELECT</b> node for a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure using Query Language Dialect 1.


## -parameters




### -param pwszRestriction

A pointer to a null-terminated string specifying an Indexing Service Query Language Dialect 1 query.


### -param ppTree

A pointer to the address of the location to receive the <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure that represents the top node of the <b>SELECT</b> part of the full command tree.


### -param cProperties

The number of properties in the <i>pProperties</i> array, or zero if <i>pProperties</i> is <b>NULL</b>.


### -param pProperties

A pointer to an array of properties that can be referred to by friendly name in <i>pwszRestriction</i>. Column names in the <b>wcsFriendlyName</b> member of each <a href="https://msdn.microsoft.com/36476b0d-7c8e-45db-b7eb-5ae710495e46">CIPROPERTYDEF</a> structure must be specified in uppercase. Indexing Service's built-in properties do not need to be defined to be used. It is an error to define a property with the same friendly name as that of a built-in property.


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



Command trees created by <b>CITextToSelectTree</b> contain the <b>SELECT</b> portion of a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure. A tree returned by <b>CITextToSelectTree</b> can be combined with project and sort nodes to form a complete command tree. Use <b>CITextToSelectTree</b> instead of the <a href="https://msdn.microsoft.com/679b96f7-43b3-44c1-86dd-e995bb9a9c53">CITextToFullTree</a> function if the sort order and project columns tree nodes are already available.

The query tree allocated by <b>CITextToSelectTree</b> must be freed either with the <a href="https://msdn.microsoft.com/8d1de2d0-6851-46a1-98fb-5b188ee57a9b">ICommandTree::FreeCommandTree</a> method or passed to the <a href="https://msdn.microsoft.com/13161978-498d-4a55-ba28-b15c66cf966f">ICommandTree::SetCommandTree</a> method with the <i>fCopy</i> parameter set to <b>FALSE</b>.


#### Examples

This example creates a <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure. A custom property from a Word document named "IssueNumber" of type "Number" is defined and used in the query.



<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DBCOMMANDTREE * pCompleteTree; 
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
                                 &amp;pSelectTree,
                                 1,
                                 aProperties,
                                 GetSystemDefaultLCID() );
if ( SUCCEEDED( hr ) )
{
    pTableNode-&gt;pctNextSibling = pSelectTree;
    hr = pICommand-&gt;SetCommandTree( pCompleteTree,
                                    DBCOMMANDREUSE_NONE,
                                    FALSE );
    if ( SUCCEEDED( hr ) )
    {
        // ...
        // execute a query
        // ...
    }
}
</pre>
</td>
</tr>
</table></span></div>
The following diagram shows the <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure pSelectTree created by the example code.



<img alt="" src="images/dbcmdtr1.png"/>
<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/36476b0d-7c8e-45db-b7eb-5ae710495e46">CIPROPERTYDEF</a>



<a href="https://msdn.microsoft.com/735074f3-0f4f-4992-8e01-8cf43ca1515a">CIRestrictionToFullTree</a>



<a href="https://msdn.microsoft.com/8d59e0f4-2c80-4d63-938b-91e7360c039b">CITextToSelectTreeEx</a>



<a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a>



<a href="https://msdn.microsoft.com/876a5c22-45bd-4b06-b323-532cd9230377">ICommandTree</a>
 

 

