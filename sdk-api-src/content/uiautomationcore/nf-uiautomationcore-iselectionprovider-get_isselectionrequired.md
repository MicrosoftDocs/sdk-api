---
UID: NF:uiautomationcore.ISelectionProvider.get_IsSelectionRequired
title: ISelectionProvider::get_IsSelectionRequired (uiautomationcore.h)
description: Indicates whether the Microsoft UI Automation provider requires at least one child element to be selected.
helpviewer_keywords: ["ISelectionProvider interface [Windows Accessibility]","IsSelectionRequired property","ISelectionProvider.IsSelectionRequired","ISelectionProvider.get_IsSelectionRequired","ISelectionProvider::IsSelectionRequired","ISelectionProvider::get_IsSelectionRequired","IsSelectionRequired property [Windows Accessibility]","IsSelectionRequired property [Windows Accessibility]","ISelectionProvider interface","get_IsSelectionRequired","uiauto.uiauto_ISelectionProvider_IsSelectionRequired","uiauto_ISelectionProvider_IsSelectionRequired","uiautomationcore/ISelectionProvider::IsSelectionRequired","uiautomationcore/ISelectionProvider::get_IsSelectionRequired","winauto.uiauto_ISelectionProvider_IsSelectionRequired"]
old-location: winauto\uiauto_ISelectionProvider_IsSelectionRequired.htm
tech.root: WinAuto
ms.assetid: 1b1ee10d-39de-480f-901f-198d9a9c48f8
ms.date: 12/05/2018
ms.keywords: ISelectionProvider interface [Windows Accessibility],IsSelectionRequired property, ISelectionProvider.IsSelectionRequired, ISelectionProvider.get_IsSelectionRequired, ISelectionProvider::IsSelectionRequired, ISelectionProvider::get_IsSelectionRequired, IsSelectionRequired property [Windows Accessibility], IsSelectionRequired property [Windows Accessibility],ISelectionProvider interface, get_IsSelectionRequired, uiauto.uiauto_ISelectionProvider_IsSelectionRequired, uiauto_ISelectionProvider_IsSelectionRequired, uiautomationcore/ISelectionProvider::IsSelectionRequired, uiautomationcore/ISelectionProvider::get_IsSelectionRequired, winauto.uiauto_ISelectionProvider_IsSelectionRequired
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
 - ISelectionProvider::get_IsSelectionRequired
 - uiautomationcore/ISelectionProvider::get_IsSelectionRequired
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
 - ISelectionProvider.IsSelectionRequired
 - ISelectionProvider.get_IsSelectionRequired
---

# ISelectionProvider::get_IsSelectionRequired


## -description

Indicates whether the Microsoft UI Automation provider requires at least one child element to be selected.
        

This property is read-only.

## -parameters

## -remarks

       
        This property can be dynamic. For example, the initial state of a control might 
        not have any items selected by default, meaning that <b>ISelectionProvider::IsSelectionRequired</b> is <b>FALSE</b>. 
        However, after an item is selected the control must always have at least one item selected.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionprovider">ISelectionProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>