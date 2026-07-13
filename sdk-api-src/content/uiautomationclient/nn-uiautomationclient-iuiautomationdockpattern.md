---
UID: NN:uiautomationclient.IUIAutomationDockPattern
title: IUIAutomationDockPattern (uiautomationclient.h)
description: Provides access to a control that enables child elements to be arranged horizontally and vertically, relative to each other.
helpviewer_keywords: ["IUIAutomationDockPattern","IUIAutomationDockPattern interface [Windows Accessibility]","IUIAutomationDockPattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationDockPattern","uiauto_IUIAutomationDockPattern","uiautomationclient/IUIAutomationDockPattern","winauto.uiauto_IUIAutomationDockPattern"]
old-location: winauto\uiauto_IUIAutomationDockPattern.htm
tech.root: WinAuto
ms.assetid: 2da816f0-9674-4b48-bb82-4eba941a7fa4
ms.date: 12/05/2018
ms.keywords: IUIAutomationDockPattern, IUIAutomationDockPattern interface [Windows Accessibility], IUIAutomationDockPattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationDockPattern, uiauto_IUIAutomationDockPattern, uiautomationclient/IUIAutomationDockPattern, winauto.uiauto_IUIAutomationDockPattern
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationDockPattern
 - uiautomationclient/IUIAutomationDockPattern
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
 - IUIAutomationDockPattern
---

# IUIAutomationDockPattern interface


## -description

Provides access to  a control that enables child elements to be arranged horizontally and vertically, relative to each other.

## -inheritance

The <b>IUIAutomationDockPattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationDockPattern</b> also has these types of members:

## -remarks

Microsoft UI Automation client applications use this interface to access the dock properties of UI Automation elements that function as controls within a docking container. A docking container is a control that allows the arrangement of child elements, both horizontally and vertically, relative to the boundaries of the docking container and other elements within the container. Controls are docked relative to each other based on their current z-order; the higher their z-order placement the farther they are placed from the specified edge of the docking container.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
