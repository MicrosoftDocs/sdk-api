---
UID: NF:uiautomationcoreapi.UiaRegisterProviderCallback
title: UiaRegisterProviderCallback function (uiautomationcoreapi.h)
description: Registers the application-defined method that is called by UI Automation to obtain a provider for an element.
helpviewer_keywords: ["UiaRegisterProviderCallback","UiaRegisterProviderCallback function [Windows Accessibility]","uiauto.uiauto_UiaRegisterProviderCallbackAutoMeth","uiauto_UiaRegisterProviderCallbackAutoMeth","uiautomationcoreapi/UiaRegisterProviderCallback","winauto.uiauto_UiaRegisterProviderCallbackAutoMeth"]
old-location: winauto\uiauto_UiaRegisterProviderCallbackAutoMeth.htm
tech.root: WinAuto
ms.assetid: f80d3f42-dc21-4790-b670-0b900f092465
ms.date: 12/05/2018
ms.keywords: UiaRegisterProviderCallback, UiaRegisterProviderCallback function [Windows Accessibility], uiauto.uiauto_UiaRegisterProviderCallbackAutoMeth, uiauto_UiaRegisterProviderCallbackAutoMeth, uiautomationcoreapi/UiaRegisterProviderCallback, winauto.uiauto_UiaRegisterProviderCallbackAutoMeth
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
 - UiaRegisterProviderCallback
 - uiautomationcoreapi/UiaRegisterProviderCallback
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
 - UiaRegisterProviderCallback
---

# UiaRegisterProviderCallback function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Registers the application-defined method that is called by UI Automation 
		to obtain a provider for an element.

## -parameters

### -param pCallback [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/nc-uiautomationcoreapi-uiaprovidercallback">UiaProviderCallback</a>*</b>

The address of the <a href="/windows/desktop/api/uiautomationcoreapi/nc-uiautomationcoreapi-uiaprovidercallback">UiaProviderCallback</a> callback function that returns the provider.