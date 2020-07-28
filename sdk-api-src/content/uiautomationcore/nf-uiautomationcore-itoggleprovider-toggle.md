---
UID: NF:uiautomationcore.IToggleProvider.Toggle
title: IToggleProvider::Toggle (uiautomationcore.h)
description: Cycles through the toggle states of a control.
helpviewer_keywords: ["IToggleProvider interface [Windows Accessibility]","Toggle method","IToggleProvider.Toggle","IToggleProvider::Toggle","Toggle","Toggle method [Windows Accessibility]","Toggle method [Windows Accessibility]","IToggleProvider interface","uiauto.uiauto_IToggleProvider_Toggle","uiauto_IToggleProvider_Toggle","uiautomationcore/IToggleProvider::Toggle","winauto.uiauto_IToggleProvider_Toggle"]
old-location: winauto\uiauto_IToggleProvider_Toggle.htm
tech.root: WinAuto
ms.assetid: afadbcaf-156f-496e-a0f3-900e7f8d44da
ms.date: 12/05/2018
ms.keywords: IToggleProvider interface [Windows Accessibility],Toggle method, IToggleProvider.Toggle, IToggleProvider::Toggle, Toggle, Toggle method [Windows Accessibility], Toggle method [Windows Accessibility],IToggleProvider interface, uiauto.uiauto_IToggleProvider_Toggle, uiauto_IToggleProvider_Toggle, uiautomationcore/IToggleProvider::Toggle, winauto.uiauto_IToggleProvider_Toggle
f1_keywords:
- uiautomationcore/IToggleProvider.Toggle
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationCore.h
api_name:
- IToggleProvider.Toggle
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IToggleProvider::Toggle


## -description


Cycles through the toggle states of a control.
        


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A control must cycle through its <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-togglestate">ToggleState</a> in this order: 
<b>ToggleState_On</b>, <b>ToggleState_Off</b> 
and, if supported, <b>ToggleState_Indeterminate</b>.
		




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itoggleprovider">IToggleProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

