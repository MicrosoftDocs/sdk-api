---
UID: NF:uiautomationcore.ISelectionProvider.get_CanSelectMultiple
title: ISelectionProvider::get_CanSelectMultiple (uiautomationcore.h)
description: Indicates whether the Microsoft UI Automation provider allows more than one child element to be selected concurrently.
helpviewer_keywords: ["CanSelectMultiple property [Windows Accessibility]","CanSelectMultiple property [Windows Accessibility]","ISelectionProvider interface","ISelectionProvider interface [Windows Accessibility]","CanSelectMultiple property","ISelectionProvider.CanSelectMultiple","ISelectionProvider.get_CanSelectMultiple","ISelectionProvider::CanSelectMultiple","ISelectionProvider::get_CanSelectMultiple","get_CanSelectMultiple","uiauto.uiauto_ISelectionProvider_CanSelectMultiple","uiauto_ISelectionProvider_CanSelectMultiple","uiautomationcore/ISelectionProvider::CanSelectMultiple","uiautomationcore/ISelectionProvider::get_CanSelectMultiple","winauto.uiauto_ISelectionProvider_CanSelectMultiple"]
old-location: winauto\uiauto_ISelectionProvider_CanSelectMultiple.htm
tech.root: WinAuto
ms.assetid: 00098f73-4cbe-4cc5-a91a-479721f9b7c1
ms.date: 12/05/2018
ms.keywords: CanSelectMultiple property [Windows Accessibility], CanSelectMultiple property [Windows Accessibility],ISelectionProvider interface, ISelectionProvider interface [Windows Accessibility],CanSelectMultiple property, ISelectionProvider.CanSelectMultiple, ISelectionProvider.get_CanSelectMultiple, ISelectionProvider::CanSelectMultiple, ISelectionProvider::get_CanSelectMultiple, get_CanSelectMultiple, uiauto.uiauto_ISelectionProvider_CanSelectMultiple, uiauto_ISelectionProvider_CanSelectMultiple, uiautomationcore/ISelectionProvider::CanSelectMultiple, uiautomationcore/ISelectionProvider::get_CanSelectMultiple, winauto.uiauto_ISelectionProvider_CanSelectMultiple
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
 - ISelectionProvider::get_CanSelectMultiple
 - uiautomationcore/ISelectionProvider::get_CanSelectMultiple
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
 - ISelectionProvider.CanSelectMultiple
 - ISelectionProvider.get_CanSelectMultiple
---

# ISelectionProvider::get_CanSelectMultiple


## -description

Indicates whether the Microsoft UI Automation provider 
        allows more than one child element to be selected concurrently.

This property is read-only.

## -parameters

## -remarks

This property may be dynamic. For example, in rare cases a control might allow 
        multiple items to be selected on initialization but subsequently allow only single selections to be made.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionprovider">ISelectionProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>