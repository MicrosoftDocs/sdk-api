---
UID: NF:uiautomationcoreapi.UiaRegisterProviderCallback
title: UiaRegisterProviderCallback function
author: windows-sdk-content
description: Registers the application-defined method that is called by UI Automation to obtain a provider for an element.
old-location: winauto\uiauto_UiaRegisterProviderCallbackAutoMeth.htm
tech.root: WinAuto
ms.assetid: f80d3f42-dc21-4790-b670-0b900f092465
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: UiaRegisterProviderCallback, UiaRegisterProviderCallback function [Windows Accessibility], uiauto.uiauto_UiaRegisterProviderCallbackAutoMeth, uiauto_UiaRegisterProviderCallbackAutoMeth, uiautomationcoreapi/UiaRegisterProviderCallback, winauto.uiauto_UiaRegisterProviderCallbackAutoMeth
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
 - UiaRegisterProviderCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaRegisterProviderCallback function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Registers the application-defined method that is called by UI Automation 
		to obtain a provider for an element.


## -parameters




### -param pCallback [in]

Type: <b><a href="https://msdn.microsoft.com/45a32e14-9b8b-452e-a2eb-0f6773980f2f">UiaProviderCallback</a>*</b>

The address of the <a href="https://msdn.microsoft.com/45a32e14-9b8b-452e-a2eb-0f6773980f2f">UiaProviderCallback</a> callback function that returns the provider.


## -returns



This function does not return a value.



