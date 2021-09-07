---
UID: NN:uiautomationcore.ITextEditProvider
title: ITextEditProvider (uiautomationcore.h)
description: Extends the ITextProvider interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.
helpviewer_keywords: ["ITextEditProvider","ITextEditProvider interface [Windows Accessibility]","ITextEditProvider interface [Windows Accessibility]","described","uiautomationcore/ITextEditProvider","winauto.uiauto_itexteditprovider"]
old-location: winauto\uiauto_itexteditprovider.htm
tech.root: WinAuto
ms.assetid: 6AA3F2A5-B34C-F7CB-13B3-6C62E2B67326
ms.date: 12/05/2018
ms.keywords: ITextEditProvider, ITextEditProvider interface [Windows Accessibility], ITextEditProvider interface [Windows Accessibility],described, uiautomationcore/ITextEditProvider, winauto.uiauto_itexteditprovider
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ITextEditProvider
 - uiautomationcore/ITextEditProvider
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
 - ITextEditProvider
---

# ITextEditProvider interface


## -description

Extends the  <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a> interface to enable Microsoft UI Automation providers to expose programmatic text-edit actions.

## -inheritance

The <b>ITextEditProvider</b> interface inherits from <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>. <b>ITextEditProvider</b> also has these types of members:

## -remarks

Call  the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent</a> function to raise the UI Automation events that notify clients of changes. Use values of <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-texteditchangetype">TextEditChangeType</a> to describe the change. Follow the guidance given in <a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a> that describes when to raise the events and what payload the events should pass to UI Automation.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/WinAuto/textedit-control-pattern">TextEdit Control Pattern</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>



<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraisetextedittextchangedevent">UiaRaiseTextEditTextChangedEvent</a>
