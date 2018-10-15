---
UID: NF:uiautomationcore.IRawElementProviderHwndOverride.GetOverrideProviderForHwnd
title: IRawElementProviderHwndOverride::GetOverrideProviderForHwnd
author: windows-sdk-content
description: Gets a UI Automation provider for the specified element.
old-location: winauto\uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd.htm
tech.root: WinAuto
ms.assetid: 595c50eb-871b-41e1-9fab-36cf3de2340f
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetOverrideProviderForHwnd, GetOverrideProviderForHwnd method [Windows Accessibility], GetOverrideProviderForHwnd method [Windows Accessibility],IRawElementProviderHwndOverride interface, IRawElementProviderHwndOverride interface [Windows Accessibility],GetOverrideProviderForHwnd method, IRawElementProviderHwndOverride.GetOverrideProviderForHwnd, IRawElementProviderHwndOverride::GetOverrideProviderForHwnd, uiauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd, uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd, uiautomationcore/IRawElementProviderHwndOverride::GetOverrideProviderForHwnd, winauto.uiauto_IRawElementProviderHwndOverride_GetOverrideProviderForHwnd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IRawElementProviderHwndOverride.GetOverrideProviderForHwnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderHwndOverride::GetOverrideProviderForHwnd


## -description


Gets a UI Automation provider for the specified element.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The window handle of the element.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives a pointer to the new provider for the specified window, or <b>NULL</b> if the provider is not being overridden. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is implemented by fragment roots that contain window-based child elements. 
			By default, controls hosted in windows are served by default providers in addition to any custom providers. 
			The default providers treat all windows within a parent window as siblings. If you want to restructure the UI Automation 
			tree so that one window-based control is seen as a child of another, you must override the default provider by implementing 
			this method on the fragment root. The returned provider can supply additional properties or override properties of the 
			specified component.

The returned provider must be part of the fragment tree. It can supply additional properties or 
			override properties of the specified component.

If the returned provider implements <a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>, 
			the provider should be part of the fragment's tree and be reachable by navigating from the fragment's root.




## -see-also




<a href="https://msdn.microsoft.com/c2aa8f29-afec-474f-8ee5-55285f06ddff">IRawElementProviderHwndOverride</a>
 

 

