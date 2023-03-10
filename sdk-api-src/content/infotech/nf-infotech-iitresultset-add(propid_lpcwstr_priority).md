---
UID: NF:infotech.IITResultSet.Add(PROPID,LPCWSTR,PRIORITY)
title: IITResultSet::Add(PROPID,LPCWSTR,PRIORITY) (infotech.h)
description: Adds a column to the result set. (overload 1/3)
helpviewer_keywords: ["Add","Add method [HTML Help Workshop]","Add method [HTML Help Workshop]","IITResultSet interface","IITResultSet interface [HTML Help Workshop]","Add method","IITResultSet.Add","IITResultSet.Add(PROPID","LPCWSTR","PRIORITY)","IITResultSet::Add","IITResultSet::Add(PROPID","LPCWSTR","PRIORITY)","htmlhelp.iitresultset_add3","infotech/IITResultSet::Add","refIITResultSetAddString"]
old-location: htmlhelp\iitresultset_add3.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitresultsetaddstring.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [HTML Help Workshop], Add method [HTML Help Workshop],IITResultSet interface, IITResultSet interface [HTML Help Workshop],Add method, IITResultSet.Add, IITResultSet.Add(PROPID,LPCWSTR,PRIORITY), IITResultSet::Add, IITResultSet::Add(PROPID,LPCWSTR,PRIORITY), htmlhelp.iitresultset_add3, infotech/IITResultSet::Add, refIITResultSetAddString
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
 - IITResultSet::Add
 - infotech/IITResultSet::Add
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
 - IITResultSet.Add
---

# IITResultSet::Add(PROPID,LPCWSTR,PRIORITY)


## -description

Adds a column to the result set.

## -parameters

### -param PropID [in]

Property ID associated with column.

### -param lpszwDefault [in]

Default value of string.

### -param Priority [in]

Download priority of column (PRIORITY_LOW, PRIORITY_NORMAL, or PRIORITY_HIGH).

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
The column was successfully added. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory allocation failed.



</td>
</tr>
</table>

## -remarks

This method is used to add a column for string properties.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitresultset">IITResultSet</a>
