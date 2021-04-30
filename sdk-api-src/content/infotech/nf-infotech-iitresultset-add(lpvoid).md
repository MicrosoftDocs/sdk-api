---
UID: NF:infotech.IITResultSet.Add(LPVOID)
title: IITResultSet::Add(LPVOID) (infotech.h)
description: Adds columns to result set, given a header containing pairs of property ID followed by property type.
helpviewer_keywords: ["Add","Add method [HTML Help Workshop]","Add method [HTML Help Workshop]","IITResultSet interface","IITResultSet interface [HTML Help Workshop]","Add method","IITResultSet.Add","IITResultSet.Add(LPVOID)","IITResultSet::Add","IITResultSet::Add(LPVOID)","htmlhelp.iitresultset_add1","infotech/IITResultSet::Add","refIITResultSetAdd"]
old-location: htmlhelp\iitresultset_add1.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitresultsetadd.htm
ms.date: 12/05/2018
ms.keywords: Add, Add method [HTML Help Workshop], Add method [HTML Help Workshop],IITResultSet interface, IITResultSet interface [HTML Help Workshop],Add method, IITResultSet.Add, IITResultSet.Add(LPVOID), IITResultSet::Add, IITResultSet::Add(LPVOID), htmlhelp.iitresultset_add1, infotech/IITResultSet::Add, refIITResultSetAdd
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

# IITResultSet::Add(LPVOID)


## -description

Adds columns to result set, given a header containing pairs of property ID followed by property type.

## -parameters

### -param lpvHdr [in]

Buffer containing property ID/property pairs.

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
The columns were successfully added.



</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitresultset">IITResultSet</a>