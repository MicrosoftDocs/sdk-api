---
UID: NF:ocidl.IPropertyPage.Activate
title: IPropertyPage::Activate (ocidl.h)
description: Creates the dialog box window for the property page.
helpviewer_keywords: ["Activate","Activate method [COM]","Activate method [COM]","IPropertyPage interface","IPropertyPage interface [COM]","Activate method","IPropertyPage.Activate","IPropertyPage::Activate","_ctrl_ipropertypage_activate","com.ipropertypage_activate","ocidl/IPropertyPage::Activate"]
old-location: com\ipropertypage_activate.htm
tech.root: com
ms.assetid: 4756d06d-0ffc-4214-9c2b-d9cb169b4337
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [COM], Activate method [COM],IPropertyPage interface, IPropertyPage interface [COM],Activate method, IPropertyPage.Activate, IPropertyPage::Activate, _ctrl_ipropertypage_activate, com.ipropertypage_activate, ocidl/IPropertyPage::Activate
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
 - IPropertyPage::Activate
 - ocidl/IPropertyPage::Activate
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
 - IPropertyPage.Activate
---

# IPropertyPage::Activate


## -description

Creates the dialog box window for the property page.

The dialog box is created without a frame, caption, or system menu/controls. The text in the dialog should match the locale obtained through <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypagesite-getlocaleid">IPropertyPageSite::GetLocaleID</a>.

## -parameters

### -param hWndParent [in]

The window handle of the parent of the dialog box that is being created.

### -param pRect [in]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the positioning information for the dialog box. This method must create its dialog box with the placement and dimensions described by this structure.

### -param bModal [in]

Indicates whether the dialog box frame is modal (<b>TRUE</b>) or modeless (<b>FALSE</b>).

## -returns

This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>prc</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property page maintains the window handle created in this process, which it uses to destroy the dialog box within <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>