---
UID: NF:ocidl.IPropertyPage.Deactivate
title: IPropertyPage::Deactivate (ocidl.h)
description: Destroys the window created in IPropertyPage::Activate.
helpviewer_keywords: ["Deactivate","Deactivate method [COM]","Deactivate method [COM]","IPropertyPage interface","IPropertyPage interface [COM]","Deactivate method","IPropertyPage.Deactivate","IPropertyPage::Deactivate","_ctrl_ipropertypage_deactivate","com.ipropertypage_deactivate","ocidl/IPropertyPage::Deactivate"]
old-location: com\ipropertypage_deactivate.htm
tech.root: com
ms.assetid: 545f7c3d-3c6f-42c2-b472-3da3bc184200
ms.date: 12/05/2018
ms.keywords: Deactivate, Deactivate method [COM], Deactivate method [COM],IPropertyPage interface, IPropertyPage interface [COM],Deactivate method, IPropertyPage.Deactivate, IPropertyPage::Deactivate, _ctrl_ipropertypage_deactivate, com.ipropertypage_deactivate, ocidl/IPropertyPage::Deactivate
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
 - IPropertyPage::Deactivate
 - ocidl/IPropertyPage::Deactivate
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
 - IPropertyPage.Deactivate
---

# IPropertyPage::Deactivate


## -description

Destroys the window created in <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a>.



## -returns

This method can return the standard return values E_UNEXPECTED and S_OK.

## -remarks

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
It is important that property pages not keep the dialog box around as an optimization. In a property sheet with many property pages, memory consumption would become excessive if all property pages kept their dialog boxes created at all times. Destroying the dialog box prevents excessive memory consumption due to a very large number of created controls in the dialog boxes. If the frame wishes to keep pages alive while they are not visible, it can use <a href="/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-show">IPropertyPage::Show</a> for that purpose. The decision is ultimately left to the frame.

E_NOTIMPL is not a valid return value.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>
