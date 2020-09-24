---
UID: NF:ocidl.IPropertyPage.Show
title: IPropertyPage::Show (ocidl.h)
description: Makes the property page dialog box visible or invisible. If the page is made visible, the page should set the focus to itself, specifically to the first property on the page.
helpviewer_keywords: ["IPropertyPage interface [COM]","Show method","IPropertyPage.Show","IPropertyPage::Show","Show","Show method [COM]","Show method [COM]","IPropertyPage interface","_ctrl_ipropertypage_show","com.ipropertypage_show","ocidl/IPropertyPage::Show"]
old-location: com\ipropertypage_show.htm
tech.root: com
ms.assetid: f89aa820-a3d3-4a41-b2b2-9ee48354fbeb
ms.date: 12/05/2018
ms.keywords: IPropertyPage interface [COM],Show method, IPropertyPage.Show, IPropertyPage::Show, Show, Show method [COM], Show method [COM],IPropertyPage interface, _ctrl_ipropertypage_show, com.ipropertypage_show, ocidl/IPropertyPage::Show
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
 - IPropertyPage::Show
 - ocidl/IPropertyPage::Show
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
 - IPropertyPage.Show
---

# IPropertyPage::Show


## -description

Makes the property page dialog box visible or invisible. If the page is made visible, the page should set the focus to itself, specifically to the first property on the page.

## -parameters

### -param nCmdShow [in]

A command describing whether to become visible (SW_SHOW or SW_SHOWNORMAL) or hidden (SW_HIDE). No other values are valid for this parameter.

## -returns

This method can return the standard return values E_INVALIDARG, E_UNEXPECTED, and S_OK.

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur after a call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a> and before a corresponding call to <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
E_NOTIMPL is not a valid return value. E_OUTOFMEMORY is not a valid return value, since no memory should be used in implementing this method.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>