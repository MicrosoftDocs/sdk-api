---
UID: NF:oleidl.IViewObject.Unfreeze
title: IViewObject::Unfreeze (oleidl.h)
description: Releases a drawing that was previously frozen using IViewObject::Freeze. The most common use of this method is for banded printing.
helpviewer_keywords: ["IViewObject interface [COM]","Unfreeze method","IViewObject.Unfreeze","IViewObject::Unfreeze","Unfreeze","Unfreeze method [COM]","Unfreeze method [COM]","IViewObject interface","_ole_iviewobject_unfreeze","com.iviewobject_unfreeze","oleidl/IViewObject::Unfreeze"]
old-location: com\iviewobject_unfreeze.htm
tech.root: com
ms.assetid: 76f3c5f6-3f29-4a89-94e2-f77489e6a744
ms.date: 12/05/2018
ms.keywords: IViewObject interface [COM],Unfreeze method, IViewObject.Unfreeze, IViewObject::Unfreeze, Unfreeze, Unfreeze method [COM], Unfreeze method [COM],IViewObject interface, _ole_iviewobject_unfreeze, com.iviewobject_unfreeze, oleidl/IViewObject::Unfreeze
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
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
 - IViewObject::Unfreeze
 - oleidl/IViewObject::Unfreeze
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IViewObject.Unfreeze
---

# IViewObject::Unfreeze


## -description

Releases a drawing that was previously frozen using <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-freeze">IViewObject::Freeze</a>. The most common use of this method is for banded printing.

## -parameters

### -param dwFreeze [in]

Contains a key previously returned from <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-freeze">IViewObject::Freeze</a> that determines which view object to unfreeze.

## -returns

This method returns S_OK on success. Other possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOCONNECTION</b></dt>
</dl>
</td>
<td width="60%">
Error in the unfreezing process or the object is currently not frozen.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-freeze">IViewObject::Freeze</a>