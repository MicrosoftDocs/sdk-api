---
UID: NF:ocidl.IPropertyPage.SetObjects
title: IPropertyPage::SetObjects (ocidl.h)
description: Provides the property page with an array of pointers to objects associated with this property page.
helpviewer_keywords: ["IPropertyPage interface [COM]","SetObjects method","IPropertyPage.SetObjects","IPropertyPage::SetObjects","SetObjects","SetObjects method [COM]","SetObjects method [COM]","IPropertyPage interface","_ctrl_ipropertypage_setobjects","com.ipropertypage_setobjects","ocidl/IPropertyPage::SetObjects"]
old-location: com\ipropertypage_setobjects.htm
tech.root: com
ms.assetid: 0d7a73ce-8e3c-40c5-9040-6370df5edc2b
ms.date: 12/05/2018
ms.keywords: IPropertyPage interface [COM],SetObjects method, IPropertyPage.SetObjects, IPropertyPage::SetObjects, SetObjects, SetObjects method [COM], SetObjects method [COM],IPropertyPage interface, _ctrl_ipropertypage_setobjects, com.ipropertypage_setobjects, ocidl/IPropertyPage::SetObjects
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
 - IPropertyPage::SetObjects
 - ocidl/IPropertyPage::SetObjects
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
 - IPropertyPage.SetObjects
---

# IPropertyPage::SetObjects


## -description

Provides the property page with an array of pointers to objects associated with this property page.

When the property page receives a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-apply">IPropertyPage::Apply</a>, it must send value changes to these objects through whatever interfaces are appropriate. The property page must query for those interfaces. This method can fail if the objects do not support the interfaces expected by the property page.

## -parameters

### -param cObjects [in]

The number of pointers in the array pointed to by <i>ppUnk</i>. If this parameter is 0, the property page must release any pointers previously passed to this method.

### -param ppUnk [in]

A pointer to an array of <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointers where each pointer identifies a unique object affected by the property sheet in which this (and possibly other) property pages are displayed. The property page must cache these pointers calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> for each pointer at that time. This array of pointers is the same one that was passed to <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframe">OleCreatePropertyFrame</a> or <a href="/windows/desktop/api/olectl/nf-olectl-olecreatepropertyframeindirect">OleCreatePropertyFrameIndirect</a> to invoke the property sheet.

## -returns

This method can return the standard return values E_FAIL, E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The property page successfully saved the pointers it needed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
One of the objects in <i>ppUnk</i> did not support the interface expected by this property page, and so this property page cannot communicate with it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>ppUnk</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The property page is required to keep the pointers returned by this method or others queried through them. If these specific <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointers are held, the property page must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> through each when caching them, until the time when <b>SetObjects</b> is called with <i>cObjects</i> equal to 0. At that time, the property page must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> through each pointer, releasing any objects that it held.



The caller must provide the property page with these objects before calling <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a>, and should call <b>SetObjects</b> with zero as the parameter when deactivating the page or when releasing the object entirely. Each call to <b>SetObjects</b> with a non-<b>NULL</b><i>ppUnk</i> parameter must be matched with a later call to <b>SetObjects</b> with 0 in the <i>cObjects</i> parameter.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>