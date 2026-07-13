---
UID: NF:infotech.IITPropList.Clear
title: IITPropList::Clear (infotech.h)
description: Clears memory associated with a property list and reinitializes the list.
helpviewer_keywords: ["Clear","Clear method [HTML Help Workshop]","Clear method [HTML Help Workshop]","IITPropList interface","IITPropList interface [HTML Help Workshop]","Clear method","IITPropList.Clear","IITPropList::Clear","htmlhelp.iitproplist_clear","infotech/IITPropList::Clear","refIITPropListClear"]
old-location: htmlhelp\iitproplist_clear.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistclear.htm
ms.date: 12/05/2018
ms.keywords: Clear, Clear method [HTML Help Workshop], Clear method [HTML Help Workshop],IITPropList interface, IITPropList interface [HTML Help Workshop],Clear method, IITPropList.Clear, IITPropList::Clear, htmlhelp.iitproplist_clear, infotech/IITPropList::Clear, refIITPropListClear
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
 - IITPropList::Clear
 - infotech/IITPropList::Clear
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
 - IITPropList.Clear
---

# IITPropList::Clear


## -description

Clears memory associated with a property list and reinitializes the list.



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
The property list was cleared.

</td>
</tr>
</table>

## -remarks

Call this method to clear a property list without requiring the list to be destroyed before it is used again.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>
