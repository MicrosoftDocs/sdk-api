---
UID: NF:ocidl.IPropertyPage2.EditProperty
title: IPropertyPage2::EditProperty (ocidl.h)
description: Specifies which field is to receive the focus when the property page is activated.
helpviewer_keywords: ["EditProperty","EditProperty method [COM]","EditProperty method [COM]","IPropertyPage2 interface","IPropertyPage2 interface [COM]","EditProperty method","IPropertyPage2.EditProperty","IPropertyPage2::EditProperty","_ctrl_ipropertypage2_editproperty","com.ipropertypage2_editproperty","ocidl/IPropertyPage2::EditProperty"]
old-location: com\ipropertypage2_editproperty.htm
tech.root: com
ms.assetid: a41d2d50-6484-43d0-a41c-1cfa3bfdbe8e
ms.date: 12/05/2018
ms.keywords: EditProperty, EditProperty method [COM], EditProperty method [COM],IPropertyPage2 interface, IPropertyPage2 interface [COM],EditProperty method, IPropertyPage2.EditProperty, IPropertyPage2::EditProperty, _ctrl_ipropertypage2_editproperty, com.ipropertypage2_editproperty, ocidl/IPropertyPage2::EditProperty
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
 - IPropertyPage2::EditProperty
 - ocidl/IPropertyPage2::EditProperty
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
 - IPropertyPage2.EditProperty
---

# IPropertyPage2::EditProperty


## -description

Specifies which field is to receive the focus when the property page is activated.

## -parameters

### -param dispID [in]

The property that is to receive the focus.

## -returns

This method can return the following values.

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not currently implemented; the interface is probably provided in anticipation of future work on this page.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If this method is called before a page is activated, the page should store the property and set the focus to it in the next call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a>. If the page is already active, <b>EditProperty</b> should set the focus to the specific property field.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage2">IPropertyPage2</a>