---
UID: NN:uiautomationcore.IProxyProviderWinEventHandler
title: IProxyProviderWinEventHandler (uiautomationcore.h)
description: Exposes a method that is implemented by proxy providers to handle WinEvents.
helpviewer_keywords: ["IProxyProviderWinEventHandler","IProxyProviderWinEventHandler interface [Windows Accessibility]","IProxyProviderWinEventHandler interface [Windows Accessibility]","described","uiauto.uiauto_IProxyProviderWinEventHandler","uiauto_IProxyProviderWinEventHandler","uiautomationcore/IProxyProviderWinEventHandler","winauto.uiauto_IProxyProviderWinEventHandler"]
old-location: winauto\uiauto_IProxyProviderWinEventHandler.htm
tech.root: WinAuto
ms.assetid: 3105ce04-fc99-494a-8db2-1a221af61c0a
ms.date: 12/05/2018
ms.keywords: IProxyProviderWinEventHandler, IProxyProviderWinEventHandler interface [Windows Accessibility], IProxyProviderWinEventHandler interface [Windows Accessibility],described, uiauto.uiauto_IProxyProviderWinEventHandler, uiauto_IProxyProviderWinEventHandler, uiautomationcore/IProxyProviderWinEventHandler, winauto.uiauto_IProxyProviderWinEventHandler
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProxyProviderWinEventHandler
 - uiautomationcore/IProxyProviderWinEventHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IProxyProviderWinEventHandler
---

# IProxyProviderWinEventHandler interface


## -description

Exposes a method that is implemented by proxy providers to handle WinEvents. To implement Microsoft UI Automation event handling, a proxy provider may need to handle WinEvents that are raised by the proxied UI. UI Automation will use the <b>IProxyProviderWinEventHandler</b> interface to notify the provider that a WinEvent has been raised for the provider window.

## -inheritance

The <b>IProxyProviderWinEventHandler</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProxyProviderWinEventHandler</b> also has these types of members:

