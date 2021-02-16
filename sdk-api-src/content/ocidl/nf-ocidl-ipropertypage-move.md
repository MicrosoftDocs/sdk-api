---
UID: NF:ocidl.IPropertyPage.Move
title: IPropertyPage::Move (ocidl.h)
description: Positions and resizes the property page dialog box within the frame.
helpviewer_keywords: ["IPropertyPage interface [COM]","Move method","IPropertyPage.Move","IPropertyPage::Move","Move","Move method [COM]","Move method [COM]","IPropertyPage interface","_ctrl_ipropertypage_move","com.ipropertypage_move","ocidl/IPropertyPage::Move"]
old-location: com\ipropertypage_move.htm
tech.root: com
ms.assetid: 305857c2-cb3a-4a56-9db3-b986b278bd02
ms.date: 12/05/2018
ms.keywords: IPropertyPage interface [COM],Move method, IPropertyPage.Move, IPropertyPage::Move, Move, Move method [COM], Move method [COM],IPropertyPage interface, _ctrl_ipropertypage_move, com.ipropertypage_move, ocidl/IPropertyPage::Move
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
 - IPropertyPage::Move
 - ocidl/IPropertyPage::Move
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
 - IPropertyPage.Move
---

# IPropertyPage::Move


## -description

Positions and resizes the property page dialog box within the frame.

## -parameters

### -param pRect [in]

A pointer to the <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure containing the positioning information for the property page dialog box.

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

The rectangle specified by <i>prc</i> is treated identically to that passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a> and before a corresponding call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The page must create its dialog box with the placement and dimensions described by this structure.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>