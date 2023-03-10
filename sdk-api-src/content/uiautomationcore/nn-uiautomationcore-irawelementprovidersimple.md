---
UID: NN:uiautomationcore.IRawElementProviderSimple
title: IRawElementProviderSimple (uiautomationcore.h)
description: Defines methods and properties that expose simple UI elements.
helpviewer_keywords: ["IRawElementProviderSimple","IRawElementProviderSimple interface [Windows Accessibility]","IRawElementProviderSimple interface [Windows Accessibility]","described","uiauto.uiauto_IRawElementProviderSimple","uiauto_IRawElementProviderSimple","uiautomationcore/IRawElementProviderSimple","winauto.uiauto_IRawElementProviderSimple"]
old-location: winauto\uiauto_IRawElementProviderSimple.htm
tech.root: WinAuto
ms.assetid: f0ec6185-acd0-4df7-88f4-fd00747f98bf
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple, IRawElementProviderSimple interface [Windows Accessibility], IRawElementProviderSimple interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderSimple, uiauto_IRawElementProviderSimple, uiautomationcore/IRawElementProviderSimple, winauto.uiauto_IRawElementProviderSimple
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
 - IRawElementProviderSimple
 - uiautomationcore/IRawElementProviderSimple
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
 - IRawElementProviderSimple
---

# IRawElementProviderSimple interface


## -description

Defines methods and properties that expose simple UI elements.

## -inheritance

The <b>IRawElementProviderSimple</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderSimple</b> also has these types of members:

## -remarks

This interface can be implemented on:
			

<ul>
<li>UI Automation provider for simple UI elements, such as buttons.</li>
<li>Providers that add or override properties or control patterns on a UI element that already has a provider.</li>
</ul>
Providers for complex elements must also implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> and, if they 
			are root elements, <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragmentroot">IRawElementProviderFragmentRoot</a>



<b>Reference</b>
