---
UID: NF:uiautomationclient.IUIAutomation6.get_ConnectionRecoveryBehavior
title: IUIAutomation6::get_ConnectionRecoveryBehavior (uiautomationclient.h)
description: Indicates whether an accessible technology client adjusts provider request timeouts when the provider is non-responsive.
helpviewer_keywords: ["ConnectionRecoveryBehavior property [Windows Accessibility]","ConnectionRecoveryBehavior property [Windows Accessibility]","IUIAutomation6 interface","IUIAutomation6 interface [Windows Accessibility]","ConnectionRecoveryBehavior property","IUIAutomation6.ConnectionRecoveryBehavior","IUIAutomation6.get_ConnectionRecoveryBehavior","IUIAutomation6::ConnectionRecoveryBehavior","IUIAutomation6::get_ConnectionRecoveryBehavior","IUIAutomation6::put_ConnectionRecoveryBehavior","get_ConnectionRecoveryBehavior","uiautomationclient/IUIAutomation6::ConnectionRecoveryBehavior","uiautomationclient/IUIAutomation6::get_ConnectionRecoveryBehavior","uiautomationclient/IUIAutomation6::put_ConnectionRecoveryBehavior","winauto.uiauto_IUIAutomation6_ConnectionRecoveryBehavior"]
old-location: winauto\uiauto_IUIAutomation6_ConnectionRecoveryBehavior.htm
tech.root: WinAuto
ms.assetid: 09184E02-1007-4F49-8B03-97430CD6327E
ms.date: 12/05/2019
ms.keywords: ConnectionRecoveryBehavior property [Windows Accessibility], ConnectionRecoveryBehavior property [Windows Accessibility],IUIAutomation6 interface, IUIAutomation6 interface [Windows Accessibility],ConnectionRecoveryBehavior property, IUIAutomation6.ConnectionRecoveryBehavior, IUIAutomation6.get_ConnectionRecoveryBehavior, IUIAutomation6::ConnectionRecoveryBehavior, IUIAutomation6::get_ConnectionRecoveryBehavior, IUIAutomation6::put_ConnectionRecoveryBehavior, get_ConnectionRecoveryBehavior, uiautomationclient/IUIAutomation6::ConnectionRecoveryBehavior, uiautomationclient/IUIAutomation6::get_ConnectionRecoveryBehavior, uiautomationclient/IUIAutomation6::put_ConnectionRecoveryBehavior, winauto.uiauto_IUIAutomation6_ConnectionRecoveryBehavior
f1_keywords:
- uiautomationclient/IUIAutomation6.ConnectionRecoveryBehavior
dev_langs:
- c++
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- UIAutomationClient.h
api_name:
- IUIAutomation6.ConnectionRecoveryBehavior
- IUIAutomation6.get_ConnectionRecoveryBehavior
- IUIAutomation6.put_ConnectionRecoveryBehavior
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
---

# IUIAutomation6::get_ConnectionRecoveryBehavior

## -description

Indicates whether an accessible technology client adjusts provider request timeouts when the provider is non-responsive.

This property is read/write.

## -remarks

> ### Parameters
>
> `connectionRecoveryBehaviorOptions` [in]
>
> Type: **ConnectionRecoveryBehaviorOptions**
>
> Value indicating whether provider request timeouts are adjusted. The default is [ConnectionRecoveryBehaviorOptions_Disabled](ne-uiautomationclient-connectionrecoverybehavioroptions.md).

## -see-also

[IUIAutomation6 interface](nn-uiautomationclient-iuiautomation6.md)
