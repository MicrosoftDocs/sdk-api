---
UID: NF:uiautomationcore.IToggleProvider.get_ToggleState
title: IToggleProvider::get_ToggleState (uiautomationcore.h)
description: Specifies the toggle state of the control.
helpviewer_keywords: ["IToggleProvider interface [Windows Accessibility]","ToggleState property","IToggleProvider.ToggleState","IToggleProvider.get_ToggleState","IToggleProvider::ToggleState","IToggleProvider::get_ToggleState","ToggleState property [Windows Accessibility]","ToggleState property [Windows Accessibility]","IToggleProvider interface","get_ToggleState","uiauto.uiauto_IToggleProvider_ToggleState","uiauto_IToggleProvider_ToggleState","uiautomationcore/IToggleProvider::ToggleState","uiautomationcore/IToggleProvider::get_ToggleState","winauto.uiauto_IToggleProvider_ToggleState"]
old-location: winauto\uiauto_IToggleProvider_ToggleState.htm
tech.root: WinAuto
ms.assetid: 57bd9b77-32f4-4abf-b942-c0fe00398e56
ms.date: 12/05/2018
ms.keywords: IToggleProvider interface [Windows Accessibility],ToggleState property, IToggleProvider.ToggleState, IToggleProvider.get_ToggleState, IToggleProvider::ToggleState, IToggleProvider::get_ToggleState, ToggleState property [Windows Accessibility], ToggleState property [Windows Accessibility],IToggleProvider interface, get_ToggleState, uiauto.uiauto_IToggleProvider_ToggleState, uiauto_IToggleProvider_ToggleState, uiautomationcore/IToggleProvider::ToggleState, uiautomationcore/IToggleProvider::get_ToggleState, winauto.uiauto_IToggleProvider_ToggleState
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
 - IToggleProvider::get_ToggleState
 - uiautomationcore/IToggleProvider::get_ToggleState
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
 - IToggleProvider.ToggleState
 - IToggleProvider.get_ToggleState
---

# IToggleProvider::get_ToggleState


## -description

Specifies the toggle state of the control.

This property is read-only.

## -parameters

## -remarks

A control must cycle through its <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-togglestate">ToggleState</a> in this order:  
<b>ToggleState_On</b>, <b>ToggleState_Off</b> 
and, if supported, <b>ToggleState_Indeterminate</b>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itoggleprovider">IToggleProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>