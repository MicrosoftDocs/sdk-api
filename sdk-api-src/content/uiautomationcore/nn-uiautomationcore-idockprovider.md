---
UID: NN:uiautomationcore.IDockProvider
title: IDockProvider (uiautomationcore.h)
description: Provides access to an element in a docking container.
helpviewer_keywords: ["IDockProvider","IDockProvider interface [Windows Accessibility]","IDockProvider interface [Windows Accessibility]","described","uiauto.uiauto_IDockProvider","uiauto_IDockProvider","uiautomationcore/IDockProvider","winauto.uiauto_IDockProvider"]
old-location: winauto\uiauto_IDockProvider.htm
tech.root: WinAuto
ms.assetid: 106ca4b4-1304-4942-88a4-79a3895b552f
ms.date: 12/05/2018
ms.keywords: IDockProvider, IDockProvider interface [Windows Accessibility], IDockProvider interface [Windows Accessibility],described, uiauto.uiauto_IDockProvider, uiauto_IDockProvider, uiautomationcore/IDockProvider, winauto.uiauto_IDockProvider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - IDockProvider
 - uiautomationcore/IDockProvider
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
 - IDockProvider
---

# IDockProvider interface


## -description

Provides access 
        to an element in a docking container.

## -inheritance

The <b>IDockProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDockProvider</b> also has these types of members:

## -remarks

<b>IDockProvider</b> does not expose any properties of the docking 
        container or any properties of controls that might be docked adjacent to the current 
        control in the docking container.
        

Controls are docked relative to each other based on their current z-order; 
        the higher their z-order placement, the farther they are placed from the specified edge of the docking container.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/WinAuto/uiauto-implementingdock">Dock Control Pattern</a>



<a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-dockposition">DockPosition</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
