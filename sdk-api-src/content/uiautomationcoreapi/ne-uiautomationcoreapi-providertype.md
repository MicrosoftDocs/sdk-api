---
UID: NE:uiautomationcoreapi.ProviderType
title: ProviderType
author: windows-sdk-content
description: Contains values that specify the type of a client-side (proxy) UI Automation provider.
old-location: winauto\uiauto_ProviderTypeEnum.htm
tech.root: WinAuto
ms.assetid: 442dcda2-046d-4203-aa55-ddf83983cb26
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: ProviderType, ProviderType enumeration [Windows Accessibility], ProviderType_BaseHwnd, ProviderType_NonClientArea, ProviderType_Proxy, uiauto.uiauto_ProviderTypeEnum, uiauto_ProviderTypeEnum, uiautomationcoreapi/ProviderType, uiautomationcoreapi/ProviderType_BaseHwnd, uiautomationcoreapi/ProviderType_NonClientArea, uiautomationcoreapi/ProviderType_Proxy, winauto.uiauto_ProviderTypeEnum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
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
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - ProviderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ProviderType enumeration


## -description


Contains values that specify the type of a client-side (proxy) UI Automation provider.


## -enum-fields




### -field ProviderType_BaseHwnd

The provider is window-based.


### -field ProviderType_Proxy

The provider is one of the Win32 or Windows Forms providers from Microsoft, or a third-party proxy provider.


### -field ProviderType_NonClientArea

The provider is a proxy for the window's non-client-area elements.

