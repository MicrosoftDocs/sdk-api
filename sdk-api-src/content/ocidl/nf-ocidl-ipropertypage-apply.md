---
UID: NF:ocidl.IPropertyPage.Apply
title: IPropertyPage::Apply (ocidl.h)
description: Applies the current values to the underlying objects associated with the property page as previously passed to IPropertyPage::SetObjects.
helpviewer_keywords: ["Apply","Apply method [COM]","Apply method [COM]","IPropertyPage interface","IPropertyPage interface [COM]","Apply method","IPropertyPage.Apply","IPropertyPage::Apply","_ctrl_ipropertypage_apply","com.ipropertypage_apply","ocidl/IPropertyPage::Apply"]
old-location: com\ipropertypage_apply.htm
tech.root: com
ms.assetid: af0a1b49-54c3-453f-bd6a-70b63d625acb
ms.date: 12/05/2018
ms.keywords: Apply, Apply method [COM], Apply method [COM],IPropertyPage interface, IPropertyPage interface [COM],Apply method, IPropertyPage.Apply, IPropertyPage::Apply, _ctrl_ipropertypage_apply, com.ipropertypage_apply, ocidl/IPropertyPage::Apply
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
 - IPropertyPage::Apply
 - ocidl/IPropertyPage::Apply
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
 - IPropertyPage.Apply
---

# IPropertyPage::Apply


## -description

Applies the current values to the underlying objects associated with the property page as previously passed to 
    <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>.



## -returns

This method can return the standard return values <b>E_OUTOFMEMORY</b> and 
      <b>E_UNEXPECTED</b>, as well as the following values.

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
Changes were successfully applied and the property page is current with the underlying objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Changes were applied, but the property page cannot determine if its state is current with the 
        objects.

</td>
</tr>
</table>

## -remarks

The objects to be changed are provided through a previous call to 
     <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-setobjects">IPropertyPage::SetObjects</a>. By calling 
     <b>IPropertyPage::SetObjects</b> prior to calling this 
     method, the caller ensures that all underlying objects have the correct interfaces through which to communicate 
     changes. Therefore, this method should not fail because of non-existent interfaces.

After applying its values, the property page should determine if its state is now current with the objects in 
     order to properly implement 
     <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-ispagedirty">IPropertyPage::IsPageDirty</a> and to provide both 
     <b>S_OK</b> and <b>S_FALSE</b> return values.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>
