---
UID: NN:uiautomationcore.IRawElementProviderSimple3
title: IRawElementProviderSimple3 (uiautomationcore.h)
description: Extends the IRawElementProviderSimple2 interface to enable retrieving metadata about how accessible technology should say the preferred content type.
helpviewer_keywords: ["IRawElementProviderSimple3","IRawElementProviderSimple3 interface [Windows Accessibility]","IRawElementProviderSimple3 interface [Windows Accessibility]","described","uiautomationcore/IRawElementProviderSimple3","winauto.uiauto_IRawElementProviderSimple3"]
old-location: winauto\uiauto_IRawElementProviderSimple3.htm
tech.root: WinAuto
ms.assetid: 33D6DD52-B6D4-4AD4-AED9-9BFA6230C86B
ms.date: 12/05/2018
ms.keywords: IRawElementProviderSimple3, IRawElementProviderSimple3 interface [Windows Accessibility], IRawElementProviderSimple3 interface [Windows Accessibility],described, uiautomationcore/IRawElementProviderSimple3, winauto.uiauto_IRawElementProviderSimple3
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IRawElementProviderSimple3
 - uiautomationcore/IRawElementProviderSimple3
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
 - IRawElementProviderSimple3
---

# IRawElementProviderSimple3 interface


## -description

Extends the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple2">IRawElementProviderSimple2</a> interface to enable retrieving metadata about how accessible technology should say the preferred content type.

## -inheritance

The <b>IRawElementProviderSimple3</b> interface inherits from <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple2">IRawElementProviderSimple2</a>. <b>IRawElementProviderSimple3</b> also has these types of members:

## -remarks

Screen reading accessibility tools like Narrator use a speech synthesizer to read what an app is showing.  Speech synthesizers usually read the provided content well based on the content description.

However, the speech synthesizer could use some help describing the preferred content type. The SayAs command provides accurate content reading from a Microsoft UI Automation provider to a UI Automation client (such as a screen reader) through UI Automation core APIs.

Examples:

<ul>
<li>Given the date 10/4, is the format Month/Day or Day/Month?
If a screen reader does not know, you could hear October 4th or 10th April. 
</li>
<li>
Given the string "10-100", is this
"Ten to one hundred" or
"Ten minus 100"?

The ability to mark the "10" as a number and the "-100" as a number helps active technology (AT) read it better.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple2">IRawElementProviderSimple2</a>
