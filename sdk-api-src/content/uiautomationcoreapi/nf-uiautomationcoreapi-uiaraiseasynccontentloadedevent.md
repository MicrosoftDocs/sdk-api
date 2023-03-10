---
UID: NF:uiautomationcoreapi.UiaRaiseAsyncContentLoadedEvent
title: UiaRaiseAsyncContentLoadedEvent function (uiautomationcoreapi.h)
description: Called by a provider to notify the Microsoft UI Automation core that content is being loaded asynchronously.
helpviewer_keywords: ["UiaRaiseAsyncContentLoadedEvent","UiaRaiseAsyncContentLoadedEvent function [Windows Accessibility]","uiauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction","uiauto_UiaRaiseAsyncContentLoadedEventFunction","uiautomationcoreapi/UiaRaiseAsyncContentLoadedEvent","winauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction"]
old-location: winauto\uiauto_UiaRaiseAsyncContentLoadedEventFunction.htm
tech.root: WinAuto
ms.assetid: 19047933-40c4-4ddb-aa95-af5cfeec44b6
ms.date: 12/05/2018
ms.keywords: UiaRaiseAsyncContentLoadedEvent, UiaRaiseAsyncContentLoadedEvent function [Windows Accessibility], uiauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction, uiauto_UiaRaiseAsyncContentLoadedEventFunction, uiautomationcoreapi/UiaRaiseAsyncContentLoadedEvent, winauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction
req.header: uiautomationcoreapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaRaiseAsyncContentLoadedEvent
 - uiautomationcoreapi/UiaRaiseAsyncContentLoadedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaRaiseAsyncContentLoadedEvent
---

# UiaRaiseAsyncContentLoadedEvent function


## -description

Called by a provider to notify the Microsoft UI Automation core that content is being loaded asynchronously.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The provider node where the content is being loaded.

### -param asyncContentLoadedState [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-asynccontentloadedstate">AsyncContentLoadedState</a></b>

The current state of loading.

### -param percentComplete [in]

Type: <b>double</b>

The percentage of content that has been loaded.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.