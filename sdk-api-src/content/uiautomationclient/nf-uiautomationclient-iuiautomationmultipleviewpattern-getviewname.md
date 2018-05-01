---
UID: NF:uiautomationclient.IUIAutomationMultipleViewPattern.GetViewName
title: IUIAutomationMultipleViewPattern::GetViewName method
author: windows-driver-content
description: Retrieves the name of a control-specific view.
old-location: winauto\uiauto_IUIAutomationMultipleViewPattern_GetViewName.htm
old-project: WinAuto
ms.assetid: cad994dc-ee7c-41a3-a878-75a79225b5f8
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetViewName method [Windows Accessibility], GetViewName method [Windows Accessibility], IUIAutomationMultipleViewPattern interface, GetViewName,IUIAutomationMultipleViewPattern.GetViewName, IUIAutomationMultipleViewPattern, IUIAutomationMultipleViewPattern interface [Windows Accessibility], GetViewName method, IUIAutomationMultipleViewPattern::GetViewName, uiauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName, uiauto_IUIAutomationMultipleViewPattern_GetViewName, uiautomationclient/IUIAutomationMultipleViewPattern::GetViewName, winauto.uiauto_IUIAutomationMultipleViewPattern_GetViewName
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationClient.h
api_name:
-	IUIAutomationMultipleViewPattern.GetViewName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationMultipleViewPattern::GetViewName method


## -description


Retrieves the name of a control-specific view.


## -parameters




### -param view [in]

Type: <b>int</b>

The identifier of the view.


### -param name [out, retval]

Type: <b>BSTR*</b>

Receives a pointer to a localized view name.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



