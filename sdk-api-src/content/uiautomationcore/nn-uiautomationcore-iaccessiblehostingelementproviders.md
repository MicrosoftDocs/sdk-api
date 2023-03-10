---
UID: NN:uiautomationcore.IAccessibleHostingElementProviders
title: IAccessibleHostingElementProviders (uiautomationcore.h)
description: A Microsoft Active Accessibility object implements this interface when the object is the root of an accessibility tree that includes windowless Microsoft ActiveX controls that implement Microsoft UI Automation.
helpviewer_keywords: ["IAccessibleHostingElementProviders","IAccessibleHostingElementProviders interface [Windows Accessibility]","IAccessibleHostingElementProviders interface [Windows Accessibility]","described","uiautomationcore/IAccessibleHostingElementProviders","winauto.iaccessiblehostingelementproviders"]
old-location: winauto\iaccessiblehostingelementproviders.htm
tech.root: WinAuto
ms.assetid: 8D974311-25CB-4D49-B907-2984D0DA58D7
ms.date: 12/05/2018
ms.keywords: IAccessibleHostingElementProviders, IAccessibleHostingElementProviders interface [Windows Accessibility], IAccessibleHostingElementProviders interface [Windows Accessibility],described, uiautomationcore/IAccessibleHostingElementProviders, winauto.iaccessiblehostingelementproviders
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
 - IAccessibleHostingElementProviders
 - uiautomationcore/IAccessibleHostingElementProviders
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
 - IAccessibleHostingElementProviders
---

# IAccessibleHostingElementProviders interface


## -description

A Microsoft Active Accessibility object implements this interface when the object is the root of an accessibility tree that includes windowless Microsoft ActiveX controls that implement Microsoft UI Automation.  Because Microsoft Active Accessibility and UI Automation use different interfaces, this interface enables a client to discover the list of hosted windowless ActiveX controls that support  UI Automation in case the client needs to treat them differently.

## -inheritance

The <b>IAccessibleHostingElementProviders</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAccessibleHostingElementProviders</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhostingaccessibles">IRawElementProviderHostingAccessibles</a>
