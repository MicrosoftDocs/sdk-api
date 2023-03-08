---
UID: NN:oleacc.IAccessibleWindowlessSite
title: IAccessibleWindowlessSite (oleacc.h)
description: A Microsoft ActiveX control site implements this interface to enable a windowless ActiveX control that has a Microsoft Active Accessibility implementation to express its accessibility.
helpviewer_keywords: ["IAccessibleWindowlessSite","IAccessibleWindowlessSite interface [Windows Accessibility]","IAccessibleWindowlessSite interface [Windows Accessibility]","described","oleacc/IAccessibleWindowlessSite","winauto.uiauto_IAccessibleWindowlessSite"]
old-location: winauto\uiauto_IAccessibleWindowlessSite.htm
tech.root: WinAuto
ms.assetid: 1ED23B39-231B-46A2-9FED-969A36DA8DD9
ms.date: 12/05/2018
ms.keywords: IAccessibleWindowlessSite, IAccessibleWindowlessSite interface [Windows Accessibility], IAccessibleWindowlessSite interface [Windows Accessibility],described, oleacc/IAccessibleWindowlessSite, winauto.uiauto_IAccessibleWindowlessSite
req.header: oleacc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Oleacc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Oleacc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAccessibleWindowlessSite
 - oleacc/IAccessibleWindowlessSite
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
 - IAccessibleWindowlessSite
---

# IAccessibleWindowlessSite interface


## -description

A Microsoft ActiveX control site implements this interface to enable a windowless ActiveX control that has a Microsoft Active Accessibility implementation to express its accessibility.    This interface enables the control container to reserve a range of object IDs that a windowless control can use to raise events, and enables the control container to provide an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> pointer for the parent of the windowless control.

## -inheritance

The <b>IAccessibleWindowlessSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessibleWindowlessSite</b> also has these types of members:

## -remarks

The functions that manage object ID ranges expect the site object to maintain a list of ranges that have already been reserved.  When the window that contains the ActiveX control receives a [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message with an <b>LPARAM</b> value (object ID) that is in a reserved range, the window should call the <a href="/windows/desktop/api/oleacc/nf-oleacc-iaccessiblehandler-accessibleobjectfromid">IAccessibleHandler::AccessibleObjectFromID</a> method to get an <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> object for that object ID.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderwindowlesssite">IRawElementProviderWindowlessSite</a>
