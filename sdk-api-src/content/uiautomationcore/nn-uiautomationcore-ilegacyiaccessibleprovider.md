---
UID: NN:uiautomationcore.ILegacyIAccessibleProvider
title: ILegacyIAccessibleProvider (uiautomationcore.h)
description: Enables Microsoft UI Automation clients to access the underlying IAccessible implementation of Microsoft Active Accessibility elements.
helpviewer_keywords: ["ILegacyIAccessibleProvider","ILegacyIAccessibleProvider interface [Windows Accessibility]","ILegacyIAccessibleProvider interface [Windows Accessibility]","described","uiauto.uiauto_ILegacyIAccessibleProvider","uiauto_ILegacyIAccessibleProvider","uiautomationcore/ILegacyIAccessibleProvider","winauto.uiauto_ILegacyIAccessibleProvider"]
old-location: winauto\uiauto_ILegacyIAccessibleProvider.htm
tech.root: WinAuto
ms.assetid: 9d911238-05d9-4bba-920f-40ca23ab9549
ms.date: 12/05/2018
ms.keywords: ILegacyIAccessibleProvider, ILegacyIAccessibleProvider interface [Windows Accessibility], ILegacyIAccessibleProvider interface [Windows Accessibility],described, uiauto.uiauto_ILegacyIAccessibleProvider, uiauto_ILegacyIAccessibleProvider, uiautomationcore/ILegacyIAccessibleProvider, winauto.uiauto_ILegacyIAccessibleProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - ILegacyIAccessibleProvider
 - uiautomationcore/ILegacyIAccessibleProvider
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
 - ILegacyIAccessibleProvider
---

# ILegacyIAccessibleProvider interface


## -description

Enables Microsoft UI Automation clients to access the underlying <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> implementation of Microsoft Active Accessibility elements.

## -inheritance

The <b>ILegacyIAccessibleProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILegacyIAccessibleProvider</b> also has these types of members:

## -remarks

This interface is implemented by the Microsoft Active Accessibility to UI Automation Proxy to expose native MSAA properties and methods to UI Automation clients that need them for legacy reasons. The proxy automatically supplies this interface for applications or controls that implement Microsoft Active Accessibility natively. This interface is not intended to be implemented by UI Automation applications or controls.
