---
UID: NN:uiautomationcore.IUIAutomationPatternInstance
title: IUIAutomationPatternInstance (uiautomationcore.h)
description: Represents a control pattern object. The client API wrapper uses this interface to implement all property and method calls in terms of the GetProperty and CallMethod methods.
helpviewer_keywords: ["IUIAutomationPatternInstance","IUIAutomationPatternInstance interface [Windows Accessibility]","IUIAutomationPatternInstance interface [Windows Accessibility]","described","uiauto.uiauto_IUIAutomationPatternInstance","uiauto_IUIAutomationPatternInstance","uiautomationcore/IUIAutomationPatternInstance","winauto.uiauto_IUIAutomationPatternInstance"]
old-location: winauto\uiauto_IUIAutomationPatternInstance.htm
tech.root: WinAuto
ms.assetid: 54791426-3905-49d6-aaaf-87a18d3ef659
ms.date: 12/05/2018
ms.keywords: IUIAutomationPatternInstance, IUIAutomationPatternInstance interface [Windows Accessibility], IUIAutomationPatternInstance interface [Windows Accessibility],described, uiauto.uiauto_IUIAutomationPatternInstance, uiauto_IUIAutomationPatternInstance, uiautomationcore/IUIAutomationPatternInstance, winauto.uiauto_IUIAutomationPatternInstance
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
 - IUIAutomationPatternInstance
 - uiautomationcore/IUIAutomationPatternInstance
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
 - IUIAutomationPatternInstance
---

# IUIAutomationPatternInstance interface


## -description

Represents a control pattern object. The client API wrapper uses this interface to implement all property and method calls in terms of the <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatterninstance-getproperty">GetProperty</a> and <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatterninstance-callmethod">CallMethod</a> methods.

## -inheritance

The <b>IUIAutomationPatternInstance</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUIAutomationPatternInstance</b> also has these types of members:

## -remarks

This interface is implemented by Microsoft UI Automation and returned by methods such as <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern">GetCurrentPattern</a>. The interface is passed to <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-iuiautomationpatternhandler-createclientwrapper">CreateClientWrapper</a>, where it is used to call the appropriate methods and property getters.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-client-controlpatterninterfaces">Control Pattern Interfaces for Clients</a>
