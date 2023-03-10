---
UID: NN:uiautomationcore.IRawElementProviderFragmentRoot
title: IRawElementProviderFragmentRoot (uiautomationcore.h)
description: Exposes methods and properties on the root element in a fragment.
helpviewer_keywords: ["IRawElementProviderFragmentRoot","IRawElementProviderFragmentRoot interface [Windows Accessibility]","IRawElementProviderFragmentRoot interface [Windows Accessibility]","described","uiauto.uiauto_IRawElementProviderFragmentRoot","uiauto_IRawElementProviderFragmentRoot","uiautomationcore/IRawElementProviderFragmentRoot","winauto.uiauto_IRawElementProviderFragmentRoot"]
old-location: winauto\uiauto_IRawElementProviderFragmentRoot.htm
tech.root: WinAuto
ms.assetid: 16e51962-915e-40ea-a7a1-6f5a5809ba05
ms.date: 12/05/2018
ms.keywords: IRawElementProviderFragmentRoot, IRawElementProviderFragmentRoot interface [Windows Accessibility], IRawElementProviderFragmentRoot interface [Windows Accessibility],described, uiauto.uiauto_IRawElementProviderFragmentRoot, uiauto_IRawElementProviderFragmentRoot, uiautomationcore/IRawElementProviderFragmentRoot, winauto.uiauto_IRawElementProviderFragmentRoot
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
 - IRawElementProviderFragmentRoot
 - uiautomationcore/IRawElementProviderFragmentRoot
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
 - IRawElementProviderFragmentRoot
---

# IRawElementProviderFragmentRoot interface


## -description

Exposes methods and properties on the root element in a fragment.

## -inheritance

The <b>IRawElementProviderFragmentRoot</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRawElementProviderFragmentRoot</b> also has these types of members:

## -remarks

This interface is implemented by a root element within a framework; for example, a list box within a window. 
			Other elements in the same fragment, such as list items, implement the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a> interface.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>



<b>Reference</b>
