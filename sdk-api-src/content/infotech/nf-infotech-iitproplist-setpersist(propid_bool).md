---
UID: NF:infotech.IITPropList.SetPersist(PROPID,BOOL)
title: IITPropList::SetPersist (infotech.h)
description: Sets the persistence state on or off for a given property.
helpviewer_keywords: ["IITPropList interface [HTML Help Workshop]","SetPersist method","IITPropList.SetPersist","IITPropList::SetPersist","IITPropList::SetPersist(PROPID","BOOL)","SetPersist","SetPersist method [HTML Help Workshop]","SetPersist method [HTML Help Workshop]","IITPropList interface","htmlhelp.iitproplist_setpersist1","infotech/IITPropList::SetPersist","refIITPropListSetPersistProperty"]
old-location: htmlhelp\iitproplist_setpersist1.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitproplistsetpersistproperty.htm
ms.date: 12/05/2018
ms.keywords: IITPropList interface [HTML Help Workshop],SetPersist method, IITPropList.SetPersist, IITPropList::SetPersist, IITPropList::SetPersist(PROPID,BOOL), SetPersist, SetPersist method [HTML Help Workshop], SetPersist method [HTML Help Workshop],IITPropList interface, htmlhelp.iitproplist_setpersist1, infotech/IITPropList::SetPersist, refIITPropListSetPersistProperty
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

# IITPropList::SetPersist


## -description

Sets the persistence state on or off for a given property.

## -parameters

### -param PropID [in]

ID of the property to set.

### -param fPersist [in]

Persistence state. If TRUE, the persistence state is on; if FALSE, the state is off.

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

## -remarks

By default, properties are created with a persistence state of TRUE.

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-iitproplist">IITPropList</a>