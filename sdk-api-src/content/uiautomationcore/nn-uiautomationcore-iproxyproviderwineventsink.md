---
UID: NN:uiautomationcore.IProxyProviderWinEventSink
title: IProxyProviderWinEventSink (uiautomationcore.h)
description: Exposes methods used by proxy providers to raise events.
helpviewer_keywords: ["IProxyProviderWinEventSink","IProxyProviderWinEventSink interface [Windows Accessibility]","IProxyProviderWinEventSink interface [Windows Accessibility]","described","uiauto.uiauto_IProxyProviderWinEventSink","uiauto_IProxyProviderWinEventSink","uiautomationcore/IProxyProviderWinEventSink","winauto.uiauto_IProxyProviderWinEventSink"]
old-location: winauto\uiauto_IProxyProviderWinEventSink.htm
tech.root: WinAuto
ms.assetid: 55489e34-ab23-4c65-9d6f-e2ff39bca74c
ms.date: 12/05/2018
ms.keywords: IProxyProviderWinEventSink, IProxyProviderWinEventSink interface [Windows Accessibility], IProxyProviderWinEventSink interface [Windows Accessibility],described, uiauto.uiauto_IProxyProviderWinEventSink, uiauto_IProxyProviderWinEventSink, uiautomationcore/IProxyProviderWinEventSink, winauto.uiauto_IProxyProviderWinEventSink
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
 - IProxyProviderWinEventSink
 - uiautomationcore/IProxyProviderWinEventSink
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
 - IProxyProviderWinEventSink
---

# IProxyProviderWinEventSink interface


## -description

Exposes methods used by proxy providers to raise events.

## -inheritance

The <b>IProxyProviderWinEventSink</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IProxyProviderWinEventSink</b> also has these types of members:

## -remarks

The <b>IProxyProviderWinEventSink</b> interface is provided by UIAutomationCore.dll when the framework calls the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iproxyproviderwineventhandler-respondtowinevent">IProxyProviderWinEventHandler::RespondToWinEvent</a> method. The framework stores the events added to the <b>IProxyProviderWinEventSink</b> object. When <b>IProxyProviderWinEventHandler::RespondToWinEvent</b> returns, the framework passes the events back to the client side, where the UI Automation events are actually fired.
