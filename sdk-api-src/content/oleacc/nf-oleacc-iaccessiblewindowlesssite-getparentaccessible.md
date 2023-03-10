---
UID: NF:oleacc.IAccessibleWindowlessSite.GetParentAccessible
title: IAccessibleWindowlessSite::GetParentAccessible (oleacc.h)
description: Retrieves an IAccessible pointer for the parent of a windowless Microsoft ActiveX control in the accessibility tree.
helpviewer_keywords: ["GetParentAccessible","GetParentAccessible method [Windows Accessibility]","GetParentAccessible method [Windows Accessibility]","IAccessibleWindowlessSite interface","IAccessibleWindowlessSite interface [Windows Accessibility]","GetParentAccessible method","IAccessibleWindowlessSite.GetParentAccessible","IAccessibleWindowlessSite::GetParentAccessible","oleacc/IAccessibleWindowlessSite::GetParentAccessible","winauto.uiauto_IAccessibleWindowlessSite_GetParentAccessible"]
old-location: winauto\uiauto_IAccessibleWindowlessSite_GetParentAccessible.htm
tech.root: WinAuto
ms.assetid: 579C2425-9C3E-4CFF-8A25-C661670FB636
ms.date: 12/05/2018
ms.keywords: GetParentAccessible, GetParentAccessible method [Windows Accessibility], GetParentAccessible method [Windows Accessibility],IAccessibleWindowlessSite interface, IAccessibleWindowlessSite interface [Windows Accessibility],GetParentAccessible method, IAccessibleWindowlessSite.GetParentAccessible, IAccessibleWindowlessSite::GetParentAccessible, oleacc/IAccessibleWindowlessSite::GetParentAccessible, winauto.uiauto_IAccessibleWindowlessSite_GetParentAccessible
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Oleacc.lib
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibleWindowlessSite::GetParentAccessible
 - oleacc/IAccessibleWindowlessSite::GetParentAccessible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccessibleWindowlessSite.GetParentAccessible
---

# IAccessibleWindowlessSite::GetParentAccessible


## -description

Retrieves an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> pointer for the parent of a windowless Microsoft ActiveX control in the accessibility tree.

## -parameters

### -param ppParent [out, optional]

Type: <b><a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a>**</b>

Receives the <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> pointer for the parent of the windowless ActiveX control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To return its parent <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object, an object that implements <b>IAccessible</b> must be able to implement the <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessible-get_accparent">get_accParent</a> method.  Implementing <b>get_accParent</b> is difficult for a   windowless  ActiveX control because the control might be unable to determine its location in the accessible tree of the parent object.  The <b>GetParentAccessible</b> method enables a windowless ActiveX control to query its site for the parent object, and then return the parent object to the client that called <b>get_accParent</b>.

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>