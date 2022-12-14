---
UID: NN:uiautomationcore.IRawElementProviderWindowlessSite
title: IRawElementProviderWindowlessSite (uiautomationcore.h)
description: A Microsoft ActiveX control site implements this interface to enable a Microsoft UI Automation-enabled ActiveX control to express its accessibility.
helpviewer_keywords: ["IRawElementProviderWindowlessSite","IRawElementProviderWindowlessSite interface [Windows Accessibility]","IRawElementProviderWindowlessSite interface [Windows Accessibility]","described","uiautomationcore/IRawElementProviderWindowlessSite","winauto.uiauto_IRawElementProviderWindowlessSite"]
old-location: winauto\uiauto_IRawElementProviderWindowlessSite.htm
tech.root: WinAuto
ms.assetid: E6BE069B-C639-4578-9E5F-8CFE1267A847
ms.date: 12/05/2018
ms.keywords: IRawElementProviderWindowlessSite, IRawElementProviderWindowlessSite interface [Windows Accessibility], IRawElementProviderWindowlessSite interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderWindowlessSite, winauto.uiauto_IRawElementProviderWindowlessSite
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderWindowlessSite
 - uiautomationcore/IRawElementProviderWindowlessSite
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderWindowlessSite
---

# IRawElementProviderWindowlessSite interface


## -description

A Microsoft ActiveX control site implements this interface to enable a Microsoft UI Automation-enabled ActiveX control to express its accessibility.   This interface enables the control container to provide an <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> pointer for the parent or siblings of the windowless ActiveX control, and to provide a runtime ID that is unique to the control site.

## -inheritance

The <b>IRawElementProviderWindowlessSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderWindowlessSite</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessiblewindowlesssite">IAccessibleWindowlessSite</a>
