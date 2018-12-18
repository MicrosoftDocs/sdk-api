---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetIAccessible
title: IUIAutomationLegacyIAccessiblePattern::GetIAccessible
author: windows-sdk-content
description: Retrieves an IAccessible object that corresponds to the Microsoft UI Automation element.
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible.htm
tech.root: WinAuto
ms.assetid: 58ce3005-dfac-4ffe-b874-69a2f994e7a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetIAccessible, GetIAccessible method [Windows Accessibility], GetIAccessible method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetIAccessible method, IUIAutomationLegacyIAccessiblePattern.GetIAccessible, IUIAutomationLegacyIAccessiblePattern::GetIAccessible, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible, uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetIAccessible, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetIAccessible
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUIAutomationLegacyIAccessiblePattern.GetIAccessible
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationLegacyIAccessiblePattern::GetIAccessible


## -description


Retrieves an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> object that corresponds to the Microsoft UI Automation element.


## -parameters




### -param ppAccessible [out, retval]

Type: <b><a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a>**</b>

Receives a pointer to an <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface for the accessible object.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns <b>NULL</b> if the underlying implementation of the UI Automation element is not a native Microsoft Active Accessibility server; that is, if a client attempts to retrieve the <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface for an element originally supported by a proxy object from OLEACC.dll, or by the UIA-to-MSAA Bridge.




## -see-also




<a href="https://msdn.microsoft.com/d6564d14-a739-47bf-9202-0757ac3ba7f8">IUIAutomationLegacyIAccessiblePattern</a>
 

 

