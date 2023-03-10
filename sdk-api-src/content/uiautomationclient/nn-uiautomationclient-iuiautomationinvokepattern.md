---
UID: NN:uiautomationclient.IUIAutomationInvokePattern
title: IUIAutomationInvokePattern (uiautomationclient.h)
description: Exposes a method that enables a client application to invoke the action of a control (typically a button).
helpviewer_keywords: ["IUIAutomationInvokePattern","IUIAutomationInvokePattern interface [Windows Accessibility]","IUIAutomationInvokePattern interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationInvokePattern","uiauto_IUIAutomationInvokePattern","uiautomationclient/IUIAutomationInvokePattern","winauto.uiauto_IUIAutomationInvokePattern"]
old-location: winauto\uiauto_IUIAutomationInvokePattern.htm
tech.root: WinAuto
ms.assetid: 08031f22-9b36-4d85-9e15-2139551b893b
ms.date: 12/05/2018
ms.keywords: IUIAutomationInvokePattern, IUIAutomationInvokePattern interface [Windows Accessibility], IUIAutomationInvokePattern interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationInvokePattern, uiauto_IUIAutomationInvokePattern, uiautomationclient/IUIAutomationInvokePattern, winauto.uiauto_IUIAutomationInvokePattern
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
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
 - IUIAutomationInvokePattern
 - uiautomationclient/IUIAutomationInvokePattern
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
 - IUIAutomationInvokePattern
---

# IUIAutomationInvokePattern interface


## -description

Exposes a method that enables a client application to invoke the action of a control (typically a button).

## -inheritance

The <b>IUIAutomationInvokePattern</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationInvokePattern</b> also has these types of members:

## -remarks

A control should support this interface if it initiates or performs a single, unambiguous action and does not maintain state when activated.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
