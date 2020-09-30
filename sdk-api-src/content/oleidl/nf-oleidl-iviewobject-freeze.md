---
UID: NF:oleidl.IViewObject.Freeze
title: IViewObject::Freeze (oleidl.h)
description: Freezes the drawn representation of an object so that it will not change until the IViewObject::Unfreeze method is called. The most common use of this method is for banded printing.
helpviewer_keywords: ["Freeze","Freeze method [COM]","Freeze method [COM]","IViewObject interface","IViewObject interface [COM]","Freeze method","IViewObject.Freeze","IViewObject::Freeze","_ole_iviewobject_freeze","com.iviewobject_freeze","oleidl/IViewObject::Freeze"]
old-location: com\iviewobject_freeze.htm
tech.root: com
ms.assetid: 943faf31-7de4-45da-887b-7ded479ac732
ms.date: 12/05/2018
ms.keywords: Freeze, Freeze method [COM], Freeze method [COM],IViewObject interface, IViewObject interface [COM],Freeze method, IViewObject.Freeze, IViewObject::Freeze, _ole_iviewobject_freeze, com.iviewobject_freeze, oleidl/IViewObject::Freeze
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
 - IViewObject::Freeze
 - oleidl/IViewObject::Freeze
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
 - IViewObject.Freeze
---

# IViewObject::Freeze


## -description

Freezes the drawn representation of an object so that it will not change until the <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-unfreeze">IViewObject::Unfreeze</a> method is called. The most common use of this method is for banded printing.

## -parameters

### -param dwDrawAspect [in]

Specifies how the object is to be represented. Representations include content, an icon, a thumbnail, or a printed document. Valid values are taken from the enumeration <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>. See the <b>DVASPECT</b> enumeration for more information.

### -param lindex [in]

Portion of the object that is of interest for the draw operation. Its interpretation varies with dwAspect. See the <a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a> enumeration for more information.

### -param pvAspect [in]

Pointer to additional information about the view of the object specified in <i>dwAspect</i>. Since none of the current aspects support additional information, <i>pvAspect</i> must always be <b>NULL</b>.

### -param pdwFreeze [out]

Pointer to where an identifying DWORD key is returned. This unique key is later used to cancel the freeze by calling <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-unfreeze">IViewObject::Unfreeze</a>. This key is an index that the default cache uses to keep track of which object is frozen.

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
<dt><b>VIEW_S_ALREADY_FROZEN</b></dt>
</dl>
</td>
<td width="60%">
Presentation has already been frozen. The value of <i>pdwFreeze</i> is the identifying key of the already frozen object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
Presentation not in cache.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_LINDEX</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>lindex</i>; currently; only -1 is supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DV_E_DVASPECT</b></dt>
</dl>
</td>
<td width="60%">
Invalid value for <i>dwAspect</i>.

</td>
</tr>
</table>

## -remarks

The <b>IViewObject::Freeze</b> method causes the view object to freeze its drawn representation until a subsequent call to <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-unfreeze">IViewObject::Unfreeze</a> releases it. After calling <b>IViewObject::Freeze</b>, successive calls to <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-draw">IViewObject::Draw</a> with the same parameters produce the same picture until <b>IViewObject::Unfreeze</b> is called.

<b>IViewObject::Freeze</b> is not part of the persistent state of the object and does not continue across unloads and reloads of the object.

The most common use of this method is for banded printing.

While in a frozen state, view notifications are not sent. Pending view notifications are deferred to the subsequent call to <a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-unfreeze">IViewObject::Unfreeze</a>.

## -see-also

<a href="/windows/desktop/api/wtypes/ne-wtypes-dvaspect">DVASPECT</a>



<a href="/windows/desktop/api/oleidl/nn-oleidl-iviewobject">IViewObject</a>



<a href="/windows/desktop/api/oleidl/nf-oleidl-iviewobject-unfreeze">IViewObject::Unfreeze</a>