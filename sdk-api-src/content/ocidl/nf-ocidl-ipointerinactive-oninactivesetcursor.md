---
UID: NF:ocidl.IPointerInactive.OnInactiveSetCursor
title: IPointerInactive::OnInactiveSetCursor (ocidl.h)
description: Sets the mouse pointer for an inactive object. This method is called by the container on receipt of a WM_SETCURSOR method when an inactive object is under the mouse pointer.
helpviewer_keywords: ["IPointerInactive interface [COM]","OnInactiveSetCursor method","IPointerInactive.OnInactiveSetCursor","IPointerInactive::OnInactiveSetCursor","OnInactiveSetCursor","OnInactiveSetCursor method [COM]","OnInactiveSetCursor method [COM]","IPointerInactive interface","_ctrl_ipointerinactive_oninactivesetcursor","com.ipointerinactive_oninactivesetcursor","ocidl/IPointerInactive::OnInactiveSetCursor"]
old-location: com\ipointerinactive_oninactivesetcursor.htm
tech.root: com
ms.assetid: f2c87f5e-5c8e-487c-ad18-ea95f334e01d
ms.date: 12/05/2018
ms.keywords: IPointerInactive interface [COM],OnInactiveSetCursor method, IPointerInactive.OnInactiveSetCursor, IPointerInactive::OnInactiveSetCursor, OnInactiveSetCursor, OnInactiveSetCursor method [COM], OnInactiveSetCursor method [COM],IPointerInactive interface, _ctrl_ipointerinactive_oninactivesetcursor, com.ipointerinactive_oninactivesetcursor, ocidl/IPointerInactive::OnInactiveSetCursor
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPointerInactive::OnInactiveSetCursor
 - ocidl/IPointerInactive::OnInactiveSetCursor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPointerInactive.OnInactiveSetCursor
---

# IPointerInactive::OnInactiveSetCursor


## -description

Sets the mouse pointer for an inactive object. This method is called by the container on receipt of a WM_SETCURSOR method when an inactive object is under the mouse pointer.

## -parameters

### -param pRectBounds [in]

The object bounding rectangle specified in client coordinate units of the containing window. This parameter tells the object its exact position and size on the screen when the WM_SETCURSOR message was received. This value is specified in units of the client's coordinate system.

### -param x [in]

The horizontal coordinate of mouse location in units of the client's containing window.

### -param y [in]

The vertical coordinate of mouse location in units of the client's containing window.

### -param dwMouseMsg [in]

The identifier of the mouse message for which a WM_SETCURSOR occurred.

### -param fSetAlways [in]

If this value is <b>TRUE</b>, the object must set the cursor; if this value is <b>FALSE</b>, the object is not obligated to set the cursor, and should return S_FALSE in that case.

## -returns

This method can return the standard return value E_FAIL, as well as the following values.

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
The mouse pointer was successfully set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The object did not set the cursor; the container should either set the cursor or call the object again with the parameter <i>fSetAlways</i> set to <b>TRUE</b>.

</td>
</tr>
</table>

## -remarks

The container calls this method to set the mouse pointer over an inactive object after checking the object's activation policy by calling the <a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-getactivationpolicy">IPointerInactive::GetActivationPolicy</a> method. If the object has not requested to be activated in-place through that call, the container dispatches subsequent WM_SETCURSOR messages to the inactive object by calling <b>OnInactiveSetCursor</b> as long as the mouse pointer stays over the object.



To avoid rounding errors and to make the job easier on the object implementer, this method takes window coordinates in the units of its containing client window, that is, the window in which the object is displayed, instead of the usual <b>HIMETRIC</b> units. Thus, the same coordinates and code path can be used when the object is active and inactive. The window coordinates specify the mouse position. The bounding rectangle is also specified in the same coordinate system.

<b>OnInactiveSetCursor</b> takes an additional parameter, <i>fSetAlways</i>, that indicates whether the object is obligated to set the cursor or not. Containers should first call this method with this parameter <b>FALSE</b>. The object may return S_FALSE to indicate that it did not set the cursor. In that case, the container should either set the cursor itself, or, if it does not wish to do this, call the <b>OnInactiveSetCursor</b> method again with <i>fSetAlways</i> being <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipointerinactive">IPointerInactive</a>