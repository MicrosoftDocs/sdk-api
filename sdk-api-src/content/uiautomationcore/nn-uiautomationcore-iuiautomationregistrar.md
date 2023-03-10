---
UID: NN:uiautomationcore.IUIAutomationRegistrar
title: IUIAutomationRegistrar (uiautomationcore.h)
description: Exposes methods for registering new control patterns, properties, and events.
helpviewer_keywords: ["IUIAutomationRegistrar","IUIAutomationRegistrar interface [Windows Accessibility]","IUIAutomationRegistrar interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationRegistrar","uiauto_IUIAutomationRegistrar","uiautomationcore/IUIAutomationRegistrar","winauto.uiauto_IUIAutomationRegistrar"]
old-location: winauto\uiauto_IUIAutomationRegistrar.htm
tech.root: WinAuto
ms.assetid: b5d979aa-7a87-4d6c-acdc-6e9eb19aac98
ms.date: 12/05/2018
ms.keywords: IUIAutomationRegistrar, IUIAutomationRegistrar interface [Windows Accessibility], IUIAutomationRegistrar interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationRegistrar, uiauto_IUIAutomationRegistrar, uiautomationcore/IUIAutomationRegistrar, winauto.uiauto_IUIAutomationRegistrar
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
 - IUIAutomationRegistrar
 - uiautomationcore/IUIAutomationRegistrar
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
 - IUIAutomationRegistrar
---

# IUIAutomationRegistrar interface


## -description

Exposes methods for registering new control patterns, properties, and events.

## -inheritance

The <b>IUIAutomationRegistrar</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationRegistrar</b> also has these types of members:

## -remarks

The **IUIAutomationRegistrar** interface is exposed by the <a href="/previous-versions/windows/desktop/legacy/ff384837(v=vs.85)">CUIAutomationRegistrar</a> object. To obtain an instance of this object, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function with a class ID of <b>CLSID_CUIAutomationRegistrar</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-entry-uiautoclientinterfaces">UI Automation Element Interfaces for Clients</a>
