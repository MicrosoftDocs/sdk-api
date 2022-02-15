---
UID: NF:uiautomationcore.IWindowProvider.SetVisualState
title: IWindowProvider::SetVisualState (uiautomationcore.h)
description: Changes the visual state of the window. For example, minimizes or maximizes it.
helpviewer_keywords: ["IWindowProvider interface [Windows Accessibility]","SetVisualState method","IWindowProvider.SetVisualState","IWindowProvider::SetVisualState","SetVisualState","SetVisualState method [Windows Accessibility]","SetVisualState method [Windows Accessibility]","IWindowProvider interface","uiauto.uiauto_IWindowProvider_SetVisualState","uiauto_IWindowProvider_SetVisualState","uiautomationcore/IWindowProvider::SetVisualState","winauto.uiauto_IWindowProvider_SetVisualState"]
old-location: winauto\uiauto_IWindowProvider_SetVisualState.htm
tech.root: WinAuto
ms.assetid: 89239900-5ee4-4f3a-a398-6ceb4846caf9
ms.date: 12/05/2018
ms.keywords: IWindowProvider interface [Windows Accessibility],SetVisualState method, IWindowProvider.SetVisualState, IWindowProvider::SetVisualState, SetVisualState, SetVisualState method [Windows Accessibility], SetVisualState method [Windows Accessibility],IWindowProvider interface, uiauto.uiauto_IWindowProvider_SetVisualState, uiauto_IWindowProvider_SetVisualState, uiautomationcore/IWindowProvider::SetVisualState, winauto.uiauto_IWindowProvider_SetVisualState
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
 - IWindowProvider::SetVisualState
 - uiautomationcore/IWindowProvider::SetVisualState
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
 - IWindowProvider.SetVisualState
---

# IWindowProvider::SetVisualState


## -description

Changes the visual state of the window. For example, minimizes or maximizes it.

## -parameters

### -param state [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-windowvisualstate">WindowVisualState</a></b>

The state of the window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iwindowprovider">IWindowProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate">WindowVisualState</a>