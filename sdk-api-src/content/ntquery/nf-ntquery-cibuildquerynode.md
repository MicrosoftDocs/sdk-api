---
UID: NF:ntquery.CIBuildQueryNode
title: CIBuildQueryNode function
author: windows-driver-content
description: Builds one node of a query restriction tree for a Command object.
old-location: indexsrv\cibuildquerynode.htm
old-project: IndexSrv
ms.assetid: VS|indexsrv|~\html\ixrefint_0c11.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: CIBuildQueryNode, CIBuildQueryNode function [Indexing Service], _idxs_CIBuildQueryNode, indexsrv.cibuildquerynode, ntquery/CIBuildQueryNode
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
req.typenames: MediaLabelInfo, *pMediaLabelInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ntquery.dll
api_name:
-	CIBuildQueryNode
product: Windows
targetos: Windows
req.lib: Ntquery.lib
req.dll: Ntquery.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# CIBuildQueryNode function


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Builds one node of a query restriction tree for a Command object.


## -parameters




### -param wcsProperty

A pointer to a null-terminated string that specifies the friendly name for a property. The friendly name can be used in an Indexing Service query, column list, or sort order.


### -param dbOperator

The operation to be performed on the node. See <a href="https://msdn.microsoft.com/564e287b-ab3c-484e-8818-1d24ba5246ce">DBCOMMANDOP</a>.


### -param pvarPropertyValue

A pointer to the <a href="_stg_propvariant">PROPVARIANT</a> structure for the value to use for the <i>wcsProperty</i> parameter.


### -param ppTree

A pointer to an output variable that receives the pointer to the <a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a> structure for the node created by this function. 



### -param cProperties

The number of properties in the <i>pProperty</i> array.


### -param pProperty

A pointer to an array of <a href="https://msdn.microsoft.com/36476b0d-7c8e-45db-b7eb-5ae710495e46">CIPROPERTYDEF</a> structures, each of which describes a property that can be referred to by a friendly name. This array is populated when <i>pvarPropertyValue</i> contains a string that contains references to properties. This parameter can be <b>NULL</b> when <i>cProperties</i> equals zero.


### -param LocaleID

The locale ID used when converting properties. The <i>pvarPropertyValue</i> parameter itself contains a string that contains references to friendly property names, which are converted to uppercase for comparison and efficiency purposes.


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
<dt><b>QPARSE_E_NO_SUCH_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The function failed because the property name specified by <i>wcsProperty</i> was not found.

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



Use nodes created by the <b>CIBuildQueryNode</b> function to create or add to a query tree using the <a href="https://msdn.microsoft.com/3c26eed6-4fca-4619-8cc5-420ce05d1e6b">CIBuildQueryTree</a> function. Content properties are in turn passed to the <a href="https://msdn.microsoft.com/333fb241-f484-4d79-89cd-9b1d8240b8a8">CITextToSelectTree</a> function to create the <b>SELECT</b> part of the full tree.




## -see-also




<a href="https://msdn.microsoft.com/3c26eed6-4fca-4619-8cc5-420ce05d1e6b">CIBuildQueryTree</a>



<a href="https://msdn.microsoft.com/679b96f7-43b3-44c1-86dd-e995bb9a9c53">CITextToFullTree</a>



<a href="https://msdn.microsoft.com/095debd6-242f-4449-b5d7-1c2cae232bf4">CITextToFullTreeEx</a>



<a href="https://msdn.microsoft.com/333fb241-f484-4d79-89cd-9b1d8240b8a8">CITextToSelectTree</a>



<a href="https://msdn.microsoft.com/8d59e0f4-2c80-4d63-938b-91e7360c039b">CITextToSelectTreeEx</a>



<a href="https://msdn.microsoft.com/564e287b-ab3c-484e-8818-1d24ba5246ce">DBCOMMANDOP</a>



<a href="https://msdn.microsoft.com/141f1952-c1b7-4fbb-81d8-7ad3e9aa9b31">DBCOMMANDTREE</a>
 

 

