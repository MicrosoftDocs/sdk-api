---
UID: NN:infotech.IITResultSet
title: IITResultSet (infotech.h)
description: Use this interface in run-time applications to initialize, build, and obtain information about result sets.
helpviewer_keywords: ["IITResultSet","IITResultSet interface [HTML Help Workshop]","IITResultSet interface [HTML Help Workshop]","described","htmlhelp.iitresultset","infotech/IITResultSet","refIITResultSetInterface"]
old-location: htmlhelp\iitresultset.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitresultsetinterface.htm
ms.date: 12/05/2018
ms.keywords: IITResultSet, IITResultSet interface [HTML Help Workshop], IITResultSet interface [HTML Help Workshop],described, htmlhelp.iitresultset, infotech/IITResultSet, refIITResultSetInterface
req.header: infotech.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IITResultSet
 - infotech/IITResultSet
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITResultSet
---

# IITResultSet interface


## -description

Use this interface in run-time applications to initialize, build, and obtain information about result sets.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITResultSet</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IITResultSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITResultSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-add(lpvoid)">Add(LPVOID)</a>
</td>
<td align="left" width="63%">
Adds columns to result set, given a header containing pairs of property ID followed by property type.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-add(propid_dword_priority)">Add(PROPID,DWORD,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-add(propid_lpcwstr_priority)">Add(PROPID,LPCWSTR,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-add(propid_lpvoid_dword_priority)">Add(PROPID,LPVOID,DWORD,PRIORITY)</a>
</td>
<td align="left" width="63%">
Adds a column to the result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-get">Get</a>
</td>
<td align="left" width="63%">
Gets the property in the specified row and column and fills the given property object.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/infotech/nf-infotech-iitresultset-getrowcount">GetRowCount</a>
</td>
<td align="left" width="63%">
Gets the number of rows in a result set.



</td>
</tr>
</table>