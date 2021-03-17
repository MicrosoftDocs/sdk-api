---
UID: NF:infotech.IITPropList.SetPersist(BOOL)
title: IITPropList::SetPersist(BOOL) (infotech.h)
description: Sets the persistence state on or off for all properties.
helpviewer_keywords: ["IITPropList interface [HTML Help Workshop]","SetPersist method","IITPropList.SetPersist","IITPropList.SetPersist(BOOL)","IITPropList::SetPersist","IITPropList::SetPersist(BOOL)","SetPersist","SetPersist method [HTML Help Workshop]","SetPersist method [HTML Help Workshop]","IITPropList interface","htmlhelp.iitproplist_setpersist2","infotech/IITPropList::SetPersist","refIITPropListSetPersist"]
old-location: htmlhelp\iitproplist_setpersist2.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsetpersist.htm
ms.date: 12/05/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SetPersist method, IITPropList.SetPersist, IITPropList.SetPersist(BOOL), IITPropList::SetPersist, IITPropList::SetPersist(BOOL), SetPersist, SetPersist method [HTML Help Workshop], SetPersist method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_setpersist2, infotech/IITPropList::SetPersist, refIITPropListSetPersist
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
 - IITPropList::SetPersist
 - infotech/IITPropList::SetPersist
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
 - IITPropList.SetPersist
---

# IITPropList::SetPersist(BOOL)


## -description

Sets the persistence state on or off for all properties.

## -parameters

### -param fPersist [in]

Persistence state. If TRUE, persistence state is on; if FALSE, the state is off.

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
The state was successfully set.



</td>
</tr>
</table>

## -remarks

By default, properties are created with a persistence state of TRUE.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>