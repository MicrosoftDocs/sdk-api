---
UID: NF:uiautomationcoreapi.UiaHasServerSideProvider
title: UiaHasServerSideProvider function
author: windows-sdk-content
description: Ascertains whether a window has a Microsoft UI Automation provider implementation.
old-location: winauto\uiauto_UiaHasServerSideProviderAutoMeth.htm
tech.root: WinAuto
ms.assetid: 0d19fccf-ebb7-469e-bb91-06c4a8803922
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: UiaHasServerSideProvider, UiaHasServerSideProvider function [Windows Accessibility], uiauto.uiauto_UiaHasServerSideProviderAutoMeth, uiauto_UiaHasServerSideProviderAutoMeth, uiautomationcoreapi/UiaHasServerSideProvider, winauto.uiauto_UiaHasServerSideProviderAutoMeth
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaHasServerSideProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaHasServerSideProvider function


## -description


Ascertains whether a window has a Microsoft UI Automation provider implementation.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

Handle of the window.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

<b>TRUE</b> if the window has a UI Automation provider implementation; otherwise <b>FALSE</b>.



