---
UID: NF:uiautomationclient.IUIAutomation2.get_ConnectionTimeout
title: IUIAutomation2::get_ConnectionTimeout (uiautomationclient.h)
description: Specifies the length of time that UI Automation will wait for a provider to respond to a client request for an automation element. (Get)
helpviewer_keywords: ["ConnectionTimeout property [Windows Accessibility]","ConnectionTimeout property [Windows Accessibility]","IUIAutomation2 interface","IUIAutomation2 interface [Windows Accessibility]","ConnectionTimeout property","IUIAutomation2.ConnectionTimeout","IUIAutomation2.get_ConnectionTimeout","IUIAutomation2::ConnectionTimeout","IUIAutomation2::get_ConnectionTimeout","IUIAutomation2::put_ConnectionTimeout","get_ConnectionTimeout","uiautomationclient/IUIAutomation2::ConnectionTimeout","uiautomationclient/IUIAutomation2::get_ConnectionTimeout","uiautomationclient/IUIAutomation2::put_ConnectionTimeout","winauto.uiauto_iuiautomation2_connectiontimeout"]
old-location: winauto\uiauto_iuiautomation2_connectiontimeout.htm
tech.root: WinAuto
ms.assetid: 636838C8-A5F6-4757-923D-2C69282B04EF
ms.date: 12/05/2018
ms.keywords: ConnectionTimeout property [Windows Accessibility], ConnectionTimeout property [Windows Accessibility],IUIAutomation2 interface, IUIAutomation2 interface [Windows Accessibility],ConnectionTimeout property, IUIAutomation2.ConnectionTimeout, IUIAutomation2.get_ConnectionTimeout, IUIAutomation2::ConnectionTimeout, IUIAutomation2::get_ConnectionTimeout, IUIAutomation2::put_ConnectionTimeout, get_ConnectionTimeout, uiautomationclient/IUIAutomation2::ConnectionTimeout, uiautomationclient/IUIAutomation2::get_ConnectionTimeout, uiautomationclient/IUIAutomation2::put_ConnectionTimeout, winauto.uiauto_iuiautomation2_connectiontimeout
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomation2::get_ConnectionTimeout
 - uiautomationclient/IUIAutomation2::get_ConnectionTimeout
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
 - IUIAutomation2.ConnectionTimeout
 - IUIAutomation2.get_ConnectionTimeout
 - IUIAutomation2.put_ConnectionTimeout
---

# IUIAutomation2::get_ConnectionTimeout


## -description

Specifies the length of time that UI Automation will wait for a provider to respond to a client request for an automation element. 

This property is read/write.

## -parameters

### -param timeout [out]

Type: <b>DWORD</b>

The duration of the time-out period, in milliseconds.

## -remarks

The default connection timeout value is two seconds. A responsive UI Automation provider can typically return an automation element to a client in a short length of time.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation2">IUIAutomation2</a>
