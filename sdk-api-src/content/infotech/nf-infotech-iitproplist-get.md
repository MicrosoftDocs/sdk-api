---
UID: NF:infotech.IITPropList.Get
title: IITPropList::Get (infotech.h)
description: Returns the property object associated with the given property ID.
helpviewer_keywords: ["Get","Get method [HTML Help Workshop]","Get method [HTML Help Workshop]","IITPropList interface","IITPropList interface [HTML Help Workshop]","Get method","IITPropList.Get","IITPropList::Get","htmlhelp.iitproplist_get","infotech/IITPropList::Get","refIITPropListGet"]
old-location: htmlhelp\iitproplist_get.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistget.htm
ms.date: 12/05/2018
ms.keywords: Get, Get method [HTML Help Workshop], Get method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],Get method, IITPropList.Get, IITPropList::Get, htmlhelp.iitproplist_get, infotech/IITPropList::Get, refIITPropListGet
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
 - IITPropList::Get
 - infotech/IITPropList::Get
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
 - IITPropList.Get
---

# IITPropList::Get


## -description

Returns the property object associated with the given property ID.

## -parameters

### -param PropID [in]

ID of the property object to get.

### -param Property [out, ref]

The property object returned.

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
The property was successfully returned.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTEXIST</b></dt>
</dl>
</td>
<td width="60%">
The requested property does not exist.



</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>