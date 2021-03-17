---
UID: NF:infotech.IITResultSet.Get
title: IITResultSet::Get (infotech.h)
description: Gets the property in the specified row and column and fills the given property object.
helpviewer_keywords: ["Get","Get method [HTML Help Workshop]","Get method [HTML Help Workshop]","IITResultSet interface","IITResultSet interface [HTML Help Workshop]","Get method","IITResultSet.Get","IITResultSet::Get","htmlhelp.iitresultset_get","infotech/IITResultSet::Get","refIITResultSetGet"]
old-location: htmlhelp\iitresultset_get.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitresultsetget.htm
ms.date: 12/05/2018
ms.keywords: Get, Get method [HTML Help Workshop], Get method [HTML Help Workshop],IITResultSet interface, IITResultSet interface [HTML Help Workshop],Get method, IITResultSet.Get, IITResultSet::Get, htmlhelp.iitresultset_get, infotech/IITResultSet::Get, refIITResultSetGet
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
 - IITResultSet::Get
 - infotech/IITResultSet::Get
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
 - IITResultSet.Get
---

# IITResultSet::Get


## -description

Gets the property in the specified row and column and fills the given property object.

## -parameters

### -param lRowIndex [in]

Row where property belongs.

### -param lColumnIndex [in]

### -param Prop [out, ref]

Column where property belongs.

## -returns

This method can return one of these values.

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
The row was successfully retrieved.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTEXIST</b></dt>
</dl>
</td>
<td width="60%">
The row or column does not exist in the row set.



</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitresultset">IITResultSet</a>