---
UID: NF:uiautomationcore.ISelectionItemProvider.Select
title: ISelectionItemProvider::Select (uiautomationcore.h)
description: Deselects any selected items and then selects the current element.
helpviewer_keywords: ["ISelectionItemProvider interface [Windows Accessibility]","Select method","ISelectionItemProvider.Select","ISelectionItemProvider::Select","Select","Select method [Windows Accessibility]","Select method [Windows Accessibility]","ISelectionItemProvider interface","uiauto.uiauto_ISelectionItemProvider_Select","uiauto_ISelectionItemProvider_Select","uiautomationcore/ISelectionItemProvider::Select","winauto.uiauto_ISelectionItemProvider_Select"]
old-location: winauto\uiauto_ISelectionItemProvider_Select.htm
tech.root: WinAuto
ms.assetid: b11e3472-e7dc-462d-93f4-e02f07ebd45f
ms.date: 12/05/2018
ms.keywords: ISelectionItemProvider interface [Windows Accessibility],Select method, ISelectionItemProvider.Select, ISelectionItemProvider::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],ISelectionItemProvider interface, uiauto.uiauto_ISelectionItemProvider_Select, uiauto_ISelectionItemProvider_Select, uiautomationcore/ISelectionItemProvider::Select, winauto.uiauto_ISelectionItemProvider_Select
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISelectionItemProvider::Select
 - uiautomationcore/ISelectionItemProvider::Select
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ISelectionItemProvider.Select
---

# ISelectionItemProvider::Select


## -description

Deselects any selected items and then selects the current element.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the current element isn’t selected, this method deselects any selected items and then selects the current element.  If the current element is already selected, this method does nothing.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
