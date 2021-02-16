---
UID: NF:oleidl.IOleObject.SetColorScheme
title: IOleObject::SetColorScheme (oleidl.h)
description: Specifies the color palette that the object application should use when it edits the specified object.
helpviewer_keywords: ["IOleObject interface [COM]","SetColorScheme method","IOleObject.SetColorScheme","IOleObject::SetColorScheme","SetColorScheme","SetColorScheme method [COM]","SetColorScheme method [COM]","IOleObject interface","_ole_ioleobject_setcolorscheme","com.ioleobject_setcolorscheme","oleidl/IOleObject::SetColorScheme"]
old-location: com\ioleobject_setcolorscheme.htm
tech.root: com
ms.assetid: 655ba4ea-941d-4389-9ee8-756dfa3c5448
ms.date: 12/05/2018
ms.keywords: IOleObject interface [COM],SetColorScheme method, IOleObject.SetColorScheme, IOleObject::SetColorScheme, SetColorScheme, SetColorScheme method [COM], SetColorScheme method [COM],IOleObject interface, _ole_ioleobject_setcolorscheme, com.ioleobject_setcolorscheme, oleidl/IOleObject::SetColorScheme
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
 - IOleObject::SetColorScheme
 - oleidl/IOleObject::SetColorScheme
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
 - IOleObject.SetColorScheme
---

# IOleObject::SetColorScheme


## -description

Specifies the color palette that the object application should use when it edits the specified object.

## -parameters

### -param pLogpal [in]

Pointer to a <a href="/windows/desktop/api/wingdi/ns-wingdi-logpalette">LOGPALETTE</a> structure that specifies the recommended palette.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Object does not support setting palettes.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_PALETTE</b></dt>
</dl>
</td>
<td width="60%">
Invalid LOGPALETTE structure pointed to by <i>pLogPal</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_NOTRUNNING</b></dt>
</dl>
</td>
<td width="60%">
Object must be running to perform this operation.

</td>
</tr>
</table>

## -remarks

The <b>IOleObject::SetColorScheme</b> method sends the container application's recommended color palette to the object application, which is not obliged to use it.

## -see-also

<a href="/windows/desktop/api/oleidl/nn-oleidl-ioleobject">IOleObject</a>