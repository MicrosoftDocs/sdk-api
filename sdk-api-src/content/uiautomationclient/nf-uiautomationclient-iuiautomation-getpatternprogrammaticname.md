---
UID: NF:uiautomationclient.IUIAutomation.GetPatternProgrammaticName
title: IUIAutomation::GetPatternProgrammaticName
author: windows-sdk-content
description: Retrieves the registered programmatic name of a control pattern.
old-location: winauto\uiauto_IUIAutomation_GetPatternProgrammaticName.htm
old-project: WinAuto
ms.assetid: a5968193-e3d9-41d1-b13f-8e86db5e0c70
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: GetPatternProgrammaticName, GetPatternProgrammaticName method [Windows Accessibility], GetPatternProgrammaticName method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],GetPatternProgrammaticName method, IUIAutomation.GetPatternProgrammaticName, IUIAutomation::GetPatternProgrammaticName, uiauto.uiauto_IUIAutomation_GetPatternProgrammaticName, uiauto_IUIAutomation_GetPatternProgrammaticName, uiautomationclient/IUIAutomation::GetPatternProgrammaticName, winauto.uiauto_IUIAutomation_GetPatternProgrammaticName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation.GetPatternProgrammaticName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomation::GetPatternProgrammaticName


## -description


Retrieves the registered programmatic name of a control pattern.


## -parameters




### -param pattern [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="https://msdn.microsoft.com/0192e840-96e6-4b12-a570-0d33a36ed885">Control Pattern Identifiers</a>.


### -param name [out, retval]

Type: <b>BSTR*</b>

Receives the registered programmatic name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The programmatic name is intended for debugging and diagnostic purposes only. The string is not localized.

This property should not be used in string comparisons. To determine whether two control patterns are the same, compare the control pattern identifiers directly.



