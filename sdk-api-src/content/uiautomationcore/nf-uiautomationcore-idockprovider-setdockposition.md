---
UID: NF:uiautomationcore.IDockProvider.SetDockPosition
title: IDockProvider::SetDockPosition (uiautomationcore.h)
description: Sets the docking position of this element.
helpviewer_keywords: ["IDockProvider interface [Windows Accessibility]","SetDockPosition method","IDockProvider.SetDockPosition","IDockProvider::SetDockPosition","SetDockPosition","SetDockPosition method [Windows Accessibility]","SetDockPosition method [Windows Accessibility]","IDockProvider interface","uiauto.uiauto_IDockProvider_SetDockPosition","uiauto_IDockProvider_SetDockPosition","uiautomationcore/IDockProvider::SetDockPosition","winauto.uiauto_IDockProvider_SetDockPosition"]
old-location: winauto\uiauto_IDockProvider_SetDockPosition.htm
tech.root: WinAuto
ms.assetid: 2e3d9a59-6bf4-4980-b318-f1badb0f8031
ms.date: 12/05/2018
ms.keywords: IDockProvider interface [Windows Accessibility],SetDockPosition method, IDockProvider.SetDockPosition, IDockProvider::SetDockPosition, SetDockPosition, SetDockPosition method [Windows Accessibility], SetDockPosition method [Windows Accessibility],IDockProvider interface, uiauto.uiauto_IDockProvider_SetDockPosition, uiauto_IDockProvider_SetDockPosition, uiautomationcore/IDockProvider::SetDockPosition, winauto.uiauto_IDockProvider_SetDockPosition
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
 - IDockProvider::SetDockPosition
 - uiautomationcore/IDockProvider::SetDockPosition
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
 - IDockProvider.SetDockPosition
---

# IDockProvider::SetDockPosition


## -description

Sets the docking position of this element.

## -parameters

### -param dockPosition [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-dockposition">DockPosition</a></b>

The new docking position.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A docking container is a control that allows the arrangement of child elements, both horizontally and vertically, relative to the boundaries of the docking container and other elements within the container.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idockprovider">IDockProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>