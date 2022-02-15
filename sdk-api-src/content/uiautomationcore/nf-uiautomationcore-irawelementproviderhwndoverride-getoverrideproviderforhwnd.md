---
UID: NF:uiautomationcore.IRawElementProviderHwndOverride.GetOverrideProviderForHwnd
title: IRawElementProviderHwndOverride::GetOverrideProviderForHwnd (uiautomationcore.h)
description: Gets a UI Automation provider for the specified element.
helpviewer_keywords: ["GetOverrideProviderForHwnd","GetOverrideProviderForHwnd method [Windows Accessibility]","GetOverrideProviderForHwnd method [Windows Accessibility]","IRawElementProviderHwndOverride interface","IRawElementProviderHwndOverride interface [Windows Accessibility]","GetOverrideProviderForHwnd method","IRawElementProviderHwndOverride.GetOverrideProviderForHwnd","IRawElementProviderHwndOverride::GetOverrideProviderForHwnd","uiauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd","uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd","uiautomationcore/IRawElementProviderHwndOverride::GetOverrideProviderForHwnd","winauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd"]
old-location: winauto\uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd.htm
tech.root: WinAuto
ms.assetid: 595c50eb-871b-41e1-9fab-36cf3de2340f
ms.date: 12/05/2018
ms.keywords: GetOverrideProviderForHwnd, GetOverrideProviderForHwnd method [Windows Accessibility], GetOverrideProviderForHwnd method [Windows Accessibility],IRawElementProviderHwndOverride interface, IRawElementProviderHwndOverride interface [Windows Accessibility],GetOverrideProviderForHwnd method, IRawElementProviderHwndOverride.GetOverrideProviderForHwnd, IRawElementProviderHwndOverride::GetOverrideProviderForHwnd, uiauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd, uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd, uiautomationcore/IRawElementProviderHwndOverride::GetOverrideProviderForHwnd, winauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd
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
 - IRawElementProviderHwndOverride::GetOverrideProviderForHwnd
 - uiautomationcore/IRawElementProviderHwndOverride::GetOverrideProviderForHwnd
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
 - IRawElementProviderHwndOverride.GetOverrideProviderForHwnd
---

# IRawElementProviderHwndOverride::GetOverrideProviderForHwnd


## -description

Gets a UI Automation provider for the specified element.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The window handle of the element.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

Receives a pointer to the new provider for the specified window, or <b>NULL</b> if the provider is not being overridden. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is implemented by fragment roots that contain window-based child elements. 
			By default, controls hosted in windows are served by default providers in addition to any custom providers. 
			The default providers treat all windows within a parent window as siblings. If you want to restructure the UI Automation 
			tree so that one window-based control is seen as a child of another, you must override the default provider by implementing 
			this method on the fragment root. The returned provider can supply additional properties or override properties of the 
			specified component.

The returned provider must be part of the fragment tree. It can supply additional properties or 
			override properties of the specified component.

If the returned provider implements <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderfragment">IRawElementProviderFragment</a>, 
			the provider should be part of the fragment's tree and be reachable by navigating from the fragment's root.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementproviderhwndoverride">IRawElementProviderHwndOverride</a>