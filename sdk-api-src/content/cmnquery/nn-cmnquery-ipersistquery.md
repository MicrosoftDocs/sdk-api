---
UID: NN:cmnquery.IPersistQuery
title: IPersistQuery (cmnquery.h)
description: Used to store and retrieve query parameters to and from persistent storage.
helpviewer_keywords: ["IPersistQuery","IPersistQuery interface [Active Directory]","IPersistQuery interface [Active Directory]","described","_glines_ipersistquery","ad.ipersistquery","cmnquery/IPersistQuery"]
old-location: ad\ipersistquery.htm
tech.root: ad
ms.assetid: 9d90f119-3d10-4f06-bed4-5ffab9ae14a4
ms.date: 12/05/2018
ms.keywords: IPersistQuery, IPersistQuery interface [Active Directory], IPersistQuery interface [Active Directory],described, _glines_ipersistquery, ad.ipersistquery, cmnquery/IPersistQuery
f1_keywords:
- cmnquery/IPersistQuery
dev_langs:
- c++
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Dsquery.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Dsquery.dll
api_name:
- IPersistQuery
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPersistQuery interface


## -description


The <b>IPersistQuery</b> interface is used to store and retrieve query parameters to and from persistent storage.This storage pertains to the query parameters, not the results of a query. A pointer to this interface is provided to a query form extension in the <a href="https://docs.microsoft.com/windows/desktop/AD/cqpm-persist">CQPM_PERSIST</a> message. An application can also provide its own  <b>IPersistQuery</b> implementation by passing a pointer to this interface to the query handler in the <b>pPersistQuery</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a> structure when <a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a> is called.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPersistQuery</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>. <b>IPersistQuery</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPersistQuery</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-clear">Clear</a>
</td>
<td align="left" width="63%">
Empties the contents of the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-readint">ReadInt</a>
</td>
<td align="left" width="63%">
Reads an integer value from the query  store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-readstring">ReadString</a>
</td>
<td align="left" width="63%">
Reads a string from the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-readstruct">ReadStruct</a>
</td>
<td align="left" width="63%">
Reads a structure from the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-writeint">WriteInt</a>
</td>
<td align="left" width="63%">
Writes an integer value to the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-writestring">WriteString</a>
</td>
<td align="left" width="63%">
Writes a string to the query store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-ipersistquery-writestruct">WriteStruct</a>
</td>
<td align="left" width="63%">
Writes a structure to the query store.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/AD/cqpm-persist">CQPM_PERSIST</a>



<a href="https://docs.microsoft.com/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/nf-cmnquery-icommonquery-openquerywindow">ICommonQuery::OpenQueryWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-ipersist">IPersist</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cmnquery/ns-cmnquery-openquerywindow">OPENQUERYWINDOW</a>
 

 

