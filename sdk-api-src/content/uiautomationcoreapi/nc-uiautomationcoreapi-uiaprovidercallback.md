---
UID: NC:uiautomationcoreapi.UiaProviderCallback
title: UiaProviderCallback
author: windows-sdk-content
description: An application-defined function that is called by UI Automation to obtain a client-side provider for an element.
old-location: winauto\uiauto_UiaProviderCallbackAutoMeth.htm
tech.root: WinAuto
ms.assetid: 45a32e14-9b8b-452e-a2eb-0f6773980f2f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UiaProviderCallback, UiaProviderCallback callback, UiaProviderCallback callback function [Windows Accessibility], uiauto.uiauto_UiaProviderCallbackAutoMeth, uiauto_UiaProviderCallbackAutoMeth, uiautomationcoreapi/UiaProviderCallback, winauto.uiauto_UiaProviderCallbackAutoMeth
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - UserDefined
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaProviderCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaProviderCallback callback function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>An application-defined function that is called by UI Automation 
		to obtain a client-side provider for an element.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window served by the provider.


### -param providerType [in]

Type: <b><a href="https://msdn.microsoft.com/442dcda2-046d-4203-aa55-ddf83983cb26">ProviderType</a></b>

A value from the <a href="https://msdn.microsoft.com/442dcda2-046d-4203-aa55-ddf83983cb26">ProviderType</a> enumerated type specifying the type of provider that is being requested.


## -returns



Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a></b>

A <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> containing the requested provider.



