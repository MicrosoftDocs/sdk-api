---
UID: NF:ocidl.IPropertyPage.SetPageSite
title: IPropertyPage::SetPageSite (ocidl.h)
description: Initializes a property page and provides the page with a pointer to the IPropertyPageSite interface through which the property page communicates with the property frame.
helpviewer_keywords: ["IPropertyPage interface [COM]","SetPageSite method","IPropertyPage.SetPageSite","IPropertyPage::SetPageSite","SetPageSite","SetPageSite method [COM]","SetPageSite method [COM]","IPropertyPage interface","_ctrl_ipropertypage_setpagesite","com.ipropertypage_setpagesite","ocidl/IPropertyPage::SetPageSite"]
old-location: com\ipropertypage_setpagesite.htm
tech.root: com
ms.assetid: a57f3f0c-53c0-4ddf-9827-df912f263a9e
ms.date: 12/05/2018
ms.keywords: IPropertyPage interface [COM],SetPageSite method, IPropertyPage.SetPageSite, IPropertyPage::SetPageSite, SetPageSite, SetPageSite method [COM], SetPageSite method [COM],IPropertyPage interface, _ctrl_ipropertypage_setpagesite, com.ipropertypage_setpagesite, ocidl/IPropertyPage::SetPageSite
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
 - IPropertyPage::SetPageSite
 - ocidl/IPropertyPage::SetPageSite
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
 - IPropertyPage.SetPageSite
---

# IPropertyPage::SetPageSite


## -description

Initializes a property page and provides the page with a pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a> interface through which the property page communicates with the property frame.

## -parameters

### -param pPageSite [in]

A pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a> interface of the page site that manages and provides services to this property page within the entire property sheet.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the <i>pPageSite</i> parameter is <b>NULL</b>, this method must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on any <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a> pointer passed during a previous call to this method. If non-<b>NULL</b>, this method must save the <b>IPropertyPageSite</b> pointer value and call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a>. Two consecutive calls to this method with a non-<b>NULL</b> site pointer are not allowed and should cause the property page to return E_UNEXPECTED.

E_NOTIMPL is not a valid return value. All property pages must implement this method.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>