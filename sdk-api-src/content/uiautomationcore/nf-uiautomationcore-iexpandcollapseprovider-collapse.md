---
UID: NF:uiautomationcore.IExpandCollapseProvider.Collapse
title: IExpandCollapseProvider::Collapse (uiautomationcore.h)
description: Hides all child nodes, controls, or content of this element.
helpviewer_keywords: ["Collapse","Collapse method [Windows Accessibility]","Collapse method [Windows Accessibility]","IExpandCollapseProvider interface","IExpandCollapseProvider interface [Windows Accessibility]","Collapse method","IExpandCollapseProvider.Collapse","IExpandCollapseProvider::Collapse","uiauto.uiauto_IExpandCollapseProvider_Collapse","uiauto_IExpandCollapseProvider_Collapse","uiautomationcore/IExpandCollapseProvider::Collapse","winauto.uiauto_IExpandCollapseProvider_Collapse"]
old-location: winauto\uiauto_IExpandCollapseProvider_Collapse.htm
tech.root: WinAuto
ms.assetid: a4915a1b-9418-4601-9333-f9508d63079a
ms.date: 12/05/2018
ms.keywords: Collapse, Collapse method [Windows Accessibility], Collapse method [Windows Accessibility],IExpandCollapseProvider interface, IExpandCollapseProvider interface [Windows Accessibility],Collapse method, IExpandCollapseProvider.Collapse, IExpandCollapseProvider::Collapse, uiauto.uiauto_IExpandCollapseProvider_Collapse, uiauto_IExpandCollapseProvider_Collapse, uiautomationcore/IExpandCollapseProvider::Collapse, winauto.uiauto_IExpandCollapseProvider_Collapse
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
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IExpandCollapseProvider::Collapse
 - uiautomationcore/IExpandCollapseProvider::Collapse
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IExpandCollapseProvider.Collapse
---

# IExpandCollapseProvider::Collapse


## -description

Hides all child nodes, controls, or content of this element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is a blocking method that returns after the element has been collapsed.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iexpandcollapseprovider">IExpandCollapseProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
