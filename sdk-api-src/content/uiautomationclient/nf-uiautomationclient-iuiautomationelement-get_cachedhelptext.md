---
UID: NF:uiautomationclient.IUIAutomationElement.get_CachedHelpText
title: IUIAutomationElement::get_CachedHelpText (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves the cached help text for the element.
old-location: winauto\uiauto_IUIAutomationElement_CachedHelpText.htm
tech.root: WinAuto
ms.assetid: 39ca5d50-808c-4a8b-a662-0a7724519b2c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CachedHelpText property [Windows Accessibility], CachedHelpText property [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],CachedHelpText property, IUIAutomationElement.CachedHelpText, IUIAutomationElement.get_CachedHelpText, IUIAutomationElement::CachedHelpText, IUIAutomationElement::get_CachedHelpText, get_CachedHelpText, uiauto.uiauto_IUIAutomationElement_CachedHelpText, uiauto_IUIAutomationElement_CachedHelpText, uiautomationclient/IUIAutomationElement::CachedHelpText, uiautomationclient/IUIAutomationElement::get_CachedHelpText, winauto.uiauto_IUIAutomationElement_CachedHelpText
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement::get_CachedHelpText


## -description


Retrieves the cached help text for the element.

This property is read-only.


## -parameters


## -remarks



This information is typically obtained from ToolTips.

<div class="alert"><b>Caution</b>  Do not retrieve the <b>CachedHelpText</b> property from a control that is based on the SysListview32 class. Doing so could cause the system to become unstable and data to be lost. A client application can discover whether a control is based on SysListview32 by retrieving the <a href="https://msdn.microsoft.com/7b5e9c75-5190-4cdd-9774-0c883747018c">CachedClassName</a> or <a href="https://msdn.microsoft.com/df019800-7467-48ef-8c16-0cb8c8d05ed5">CurrentClassName</a> property from the control.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f7613ad1-0b75-46fb-b9ac-b1ae9eea4193">Automation Element Property IDs</a>



<a href="https://msdn.microsoft.com/02ecfecc-5c3d-458b-827a-a598b8f98916">CurrentHelpText</a>



<a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>



<b>Reference</b>
 

 

