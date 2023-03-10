---
UID: NF:olectl.OleCreatePropertyFrame
title: OleCreatePropertyFrame function (olectl.h)
description: Invokes a new property frame, that is, a property sheet dialog box, whose parent is hwndOwner, where the dialog is positioned at the point (x,y) in the parent window and has the caption lpszCaption.
helpviewer_keywords: ["OleCreatePropertyFrame","OleCreatePropertyFrame function [COM]","_ctrl_OleCreatePropertyFrame","com.olecreatepropertyframe","olectl/OleCreatePropertyFrame"]
old-location: com\olecreatepropertyframe.htm
tech.root: com
ms.assetid: 06f75ac2-3ee6-4209-83cf-a4e5244a18bd
ms.date: 12/05/2018
ms.keywords: OleCreatePropertyFrame, OleCreatePropertyFrame function [COM], _ctrl_OleCreatePropertyFrame, com.olecreatepropertyframe, olectl/OleCreatePropertyFrame
req.header: olectl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OleCreatePropertyFrame
 - olectl/OleCreatePropertyFrame
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - OleCreatePropertyFrame
---

# OleCreatePropertyFrame function


## -description

Invokes a new property frame, that is, a property sheet dialog box, whose parent is <i>hwndOwner</i>, where the dialog is positioned at the point (x,y) in the parent window and has the caption <i>lpszCaption</i>.

## -parameters

### -param hwndOwner [in]

Handle to the parent window of the resulting property sheet dialog box.

### -param x [in]

Reserved. Horizontal position for the dialog box relative to <i>hwndOwner</i>.

### -param y [in]

Reserved. Vertical position for the dialog box relative to <i>hwndOwner</i>.

### -param lpszCaption [in]

Pointer to the string used for the caption of the dialog box.

### -param cObjects [in]

Number of object pointers passed in <i>ppUnk</i>.

### -param ppUnk [in]

An array of <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers on the objects for which this property sheet is being invoked. The number of elements in the array is specified by <i>cObjects</i>. These pointers are passed to each property page through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>.

### -param cPages [in]

Number of property pages specified in <i>pPageCIsID</i>.

### -param pPageClsID [in]

Array of size <i>cPages</i> containing the CLSIDs of each property page to display in the property sheet.

### -param lcid [in]

Locale identifier to use for the property sheet. Property pages can retrieve this identifier through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>.

### -param dwReserved [in]

Reserved for future use; must be zero.

### -param pvReserved [in]

Reserved for future use; must be <b>NULL</b>.

## -returns

This function supports the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following: 

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
The dialog box was invoked and operated successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>lpszCaption</i>, <i>ppUnk</i>, or <i>pPageCIsID</i> is not valid. For example, any one of them may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property pages to be displayed are identified with <i>pPageClsID</i>, which is an array of <i>cPages</i> <a href="/windows/desktop/com/clsid">CLSID</a> values. The objects that are affected by this property sheet are identified in <i>ppUnk</i>, an array of size <i>cObjects</i> containing <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers.

This function always creates a modal dialog box and does not return until the dialog box is closed.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>



<a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>