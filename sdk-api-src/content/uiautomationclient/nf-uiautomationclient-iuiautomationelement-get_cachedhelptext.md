---
UID: NF:uiautomationclient.IUIAutomationElement.get_CachedHelpText
title: IUIAutomationElement::get_CachedHelpText (uiautomationclient.h)
description: Retrieves the cached help text for the element.
helpviewer_keywords: ["CachedHelpText property [Windows Accessibility]","CachedHelpText property [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","CachedHelpText property","IUIAutomationElement.CachedHelpText","IUIAutomationElement.get_CachedHelpText","IUIAutomationElement::CachedHelpText","IUIAutomationElement::get_CachedHelpText","get_CachedHelpText","uiauto.uiauto_IUIAutomationElement_CachedHelpText","uiauto_IUIAutomationElement_CachedHelpText","uiautomationclient/IUIAutomationElement::CachedHelpText","uiautomationclient/IUIAutomationElement::get_CachedHelpText","winauto.uiauto_IUIAutomationElement_CachedHelpText"]
old-location: winauto\uiauto_IUIAutomationElement_CachedHelpText.htm
tech.root: WinAuto
ms.assetid: 39ca5d50-808c-4a8b-a662-0a7724519b2c
ms.date: 12/05/2018
ms.keywords: CachedHelpText property [Windows Accessibility], CachedHelpText property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CachedHelpText property, IUIAutomationElement.CachedHelpText, IUIAutomationElement.get_CachedHelpText, IUIAutomationElement::CachedHelpText, IUIAutomationElement::get_CachedHelpText, get_CachedHelpText, uiauto.uiauto_IUIAutomationElement_CachedHelpText, uiauto_IUIAutomationElement_CachedHelpText, uiautomationclient/IUIAutomationElement::CachedHelpText, uiautomationclient/IUIAutomationElement::get_CachedHelpText, winauto.uiauto_IUIAutomationElement_CachedHelpText
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationElement::get_CachedHelpText
 - uiautomationclient/IUIAutomationElement::get_CachedHelpText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationElement.CachedHelpText
 - IUIAutomationElement.get_CachedHelpText
---

# IUIAutomationElement::get_CachedHelpText


## -description

Retrieves the cached help text for the element.

This property is read-only.

## -parameters

## -remarks

This information is typically obtained from ToolTips.

<div class="alert"><b>Caution</b>  Do not retrieve the <b>CachedHelpText</b> property from a control that is based on the SysListview32 class. Doing so could cause the system to become unstable and data to be lost. A client application can discover whether a control is based on SysListview32 by retrieving the <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_cachedclassname">CachedClassName</a> or <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currentclassname">CurrentClassName</a> property from the control.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext">CurrentHelpText</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>