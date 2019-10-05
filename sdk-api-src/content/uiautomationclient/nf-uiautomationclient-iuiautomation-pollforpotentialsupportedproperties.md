---
UID: NF:uiautomationclient.IUIAutomation.PollForPotentialSupportedProperties
title: IUIAutomation::PollForPotentialSupportedProperties (uiautomationclient.h)
author: windows-sdk-content
description: Retrieves the properties that might be supported on a UI Automation element.
old-location: winauto\uiauto_IUIAutomation_PollForPotentialSupportedProperties.htm
tech.root: WinAuto
ms.assetid: 2cb78604-3c61-4362-9d8a-e40d5ddb4047
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IUIAutomation interface [Windows Accessibility],PollForPotentialSupportedProperties method, IUIAutomation.PollForPotentialSupportedProperties, IUIAutomation::PollForPotentialSupportedProperties, PollForPotentialSupportedProperties, PollForPotentialSupportedProperties method [Windows Accessibility], PollForPotentialSupportedProperties method [Windows Accessibility],IUIAutomation interface, uiauto.uiauto_IUIAutomation_PollForPotentialSupportedProperties, uiauto_IUIAutomation_PollForPotentialSupportedProperties, uiautomationclient/IUIAutomation::PollForPotentialSupportedProperties, winauto.uiauto_IUIAutomation_PollForPotentialSupportedProperties
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomation.PollForPotentialSupportedProperties"
dev_langs:
 - c++
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
 - IUIAutomation.PollForPotentialSupportedProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomation::PollForPotentialSupportedProperties


## -description


Retrieves the properties that might be supported on a UI Automation element.


## -parameters




### -param pElement [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

The address of the UI Automation element to poll.


### -param propertyIds [out]

Type: <b>SAFEARRAY(int)**</b>

Receives a pointer to an array of property identifiers.  For a list of property IDs, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.


### -param propertyNames [out]

Type: <b>SAFEARRAY(BSTR)**</b>

Receives a pointer to an array of property names.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is intended only for use by Microsoft UI Automation tools that need to scan for properties and control patterns. It is not intended to be used by UI Automation clients.

There is no guarantee that the element will support any particular property when asked for it later.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-custompropertieseventscontrolpatterns">Custom Properties, Events, and Control Patterns</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-pollforpotentialsupportedpatterns">PollForPotentialSupportedPatterns</a>



<b>Reference</b>
 

 

