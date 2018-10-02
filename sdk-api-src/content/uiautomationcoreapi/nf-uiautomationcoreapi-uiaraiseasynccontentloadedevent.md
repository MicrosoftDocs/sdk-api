---
UID: NF:uiautomationcoreapi.UiaRaiseAsyncContentLoadedEvent
title: UiaRaiseAsyncContentLoadedEvent function
author: windows-sdk-content
description: Called by a provider to notify the Microsoft UI Automation core that content is being loaded asynchronously.
old-location: winauto\uiauto_UiaRaiseAsyncContentLoadedEventFunction.htm
tech.root: WinAuto
ms.assetid: 19047933-40c4-4ddb-aa95-af5cfeec44b6
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: UiaRaiseAsyncContentLoadedEvent, UiaRaiseAsyncContentLoadedEvent function [Windows Accessibility], uiauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction, uiauto_UiaRaiseAsyncContentLoadedEventFunction, uiautomationcoreapi/UiaRaiseAsyncContentLoadedEvent, winauto.uiauto_UiaRaiseAsyncContentLoadedEventFunction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaRaiseAsyncContentLoadedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRaiseAsyncContentLoadedEvent function


## -description


Called by a provider to notify the Microsoft UI Automation core that content is being loaded asynchronously.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider node where the content is being loaded.


### -param asyncContentLoadedState [in]

Type: <b><a href="https://msdn.microsoft.com/7c562d3a-10cc-4d9e-aaad-6729574fcb96">AsyncContentLoadedState</a></b>

The current state of loading.


### -param percentComplete [in]

Type: <b>double</b>

The percentage of content that has been loaded.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



