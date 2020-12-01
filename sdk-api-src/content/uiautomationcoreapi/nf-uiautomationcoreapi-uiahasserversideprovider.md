---
UID: NF:uiautomationcoreapi.UiaHasServerSideProvider
title: UiaHasServerSideProvider function (uiautomationcoreapi.h)
description: Ascertains whether a window has a Microsoft UI Automation provider implementation.
helpviewer_keywords: ["UiaHasServerSideProvider","UiaHasServerSideProvider function [Windows Accessibility]","uiauto.uiauto_UiaHasServerSideProviderAutoMeth","uiauto_UiaHasServerSideProviderAutoMeth","uiautomationcoreapi/UiaHasServerSideProvider","winauto.uiauto_UiaHasServerSideProviderAutoMeth"]
old-location: winauto\uiauto_UiaHasServerSideProviderAutoMeth.htm
tech.root: WinAuto
ms.assetid: 0d19fccf-ebb7-469e-bb91-06c4a8803922
ms.date: 12/05/2018
ms.keywords: UiaHasServerSideProvider, UiaHasServerSideProvider function [Windows Accessibility], uiauto.uiauto_UiaHasServerSideProviderAutoMeth, uiauto_UiaHasServerSideProviderAutoMeth, uiautomationcoreapi/UiaHasServerSideProvider, winauto.uiauto_UiaHasServerSideProviderAutoMeth
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaHasServerSideProvider
 - uiautomationcoreapi/UiaHasServerSideProvider
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
 - UiaHasServerSideProvider
---

# UiaHasServerSideProvider function


## -description

Ascertains whether a window has a Microsoft UI Automation provider implementation.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

Handle of the window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the window has a UI Automation provider implementation; otherwise <b>FALSE</b>.