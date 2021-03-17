---
UID: NC:uiautomationcoreapi.UiaProviderCallback
title: UiaProviderCallback (uiautomationcoreapi.h)
description: An application-defined function that is called by UI Automation to obtain a client-side provider for an element.
helpviewer_keywords: ["UiaProviderCallback","UiaProviderCallback callback","UiaProviderCallback callback function [Windows Accessibility]","uiauto.uiauto_UiaProviderCallbackAutoMeth","uiauto_UiaProviderCallbackAutoMeth","uiautomationcoreapi/UiaProviderCallback","winauto.uiauto_UiaProviderCallbackAutoMeth"]
old-location: winauto\uiauto_UiaProviderCallbackAutoMeth.htm
tech.root: WinAuto
ms.assetid: 45a32e14-9b8b-452e-a2eb-0f6773980f2f
ms.date: 12/05/2018
ms.keywords: UiaProviderCallback, UiaProviderCallback callback, UiaProviderCallback callback function [Windows Accessibility], uiauto.uiauto_UiaProviderCallbackAutoMeth, uiauto_UiaProviderCallbackAutoMeth, uiautomationcoreapi/UiaProviderCallback, winauto.uiauto_UiaProviderCallbackAutoMeth
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaProviderCallback
 - uiautomationcoreapi/UiaProviderCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaProviderCallback
---

# UiaProviderCallback callback function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>An application-defined function that is called by UI Automation 
		to obtain a client-side provider for an element.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window served by the provider.

### -param providerType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-providertype">ProviderType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-providertype">ProviderType</a> enumerated type specifying the type of provider that is being requested.

## -returns

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a></b>

A <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> containing the requested provider.