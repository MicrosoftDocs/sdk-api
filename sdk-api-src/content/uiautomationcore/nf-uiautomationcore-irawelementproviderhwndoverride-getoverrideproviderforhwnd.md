---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

