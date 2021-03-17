---
UID: NF:ocidl.IPropertyPage.TranslateAccelerator
title: IPropertyPage::TranslateAccelerator (ocidl.h)
description: Passes a keystroke to the property page for processing.
helpviewer_keywords: ["IPropertyPage interface [COM]","TranslateAccelerator method","IPropertyPage.TranslateAccelerator","IPropertyPage::TranslateAccelerator","TranslateAccelerator","TranslateAccelerator method [COM]","TranslateAccelerator method [COM]","IPropertyPage interface","_ctrl_ipropertypage_translateaccelerator","com.ipropertypage_translateaccelerator","ocidl/IPropertyPage::TranslateAccelerator"]
old-location: com\ipropertypage_translateaccelerator.htm
tech.root: com
ms.assetid: 70501c3d-257c-4981-b841-4bd45f0bec27
ms.date: 12/05/2018
ms.keywords: IPropertyPage interface [COM],TranslateAccelerator method, IPropertyPage.TranslateAccelerator, IPropertyPage::TranslateAccelerator, TranslateAccelerator, TranslateAccelerator method [COM], TranslateAccelerator method [COM],IPropertyPage interface, _ctrl_ipropertypage_translateaccelerator, com.ipropertypage_translateaccelerator, ocidl/IPropertyPage::TranslateAccelerator
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
 - IPropertyPage::TranslateAccelerator
 - ocidl/IPropertyPage::TranslateAccelerator
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
 - IPropertyPage.TranslateAccelerator
---

# IPropertyPage::TranslateAccelerator


## -description

Passes a keystroke to the property page for processing.

## -parameters

### -param pMsg [in]

A pointer to the <a href="/windows/desktop/api/winuser/ns-winuser-msg">MSG</a> structure describing the keystroke to be processed.

## -returns

This method can return the standard return value E_UNEXPECTED, as well as the following values.

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
The property page handles the accelerator.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The property page handles accelerators, but this one was not useful to it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The property page does not handle accelerators.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pMsg</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a> and before the corresponding call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">IPropertyPage::Deactivate</a>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>