---
UID: NF:uiautomationclient.IUIAutomationValuePattern.SetValue
title: IUIAutomationValuePattern::SetValue method
author: windows-driver-content
description: Sets the value of the element.
old-location: winauto\uiauto_IUIAutomationValuePattern_SetValue.htm
old-project: WinAuto
ms.assetid: 9b4caa59-bda4-4cc6-b2d8-ff47ea292746
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: IUIAutomationValuePattern, IUIAutomationValuePattern interface [Windows Accessibility], SetValue method, IUIAutomationValuePattern::SetValue, SetValue method [Windows Accessibility], SetValue method [Windows Accessibility], IUIAutomationValuePattern interface, SetValue,IUIAutomationValuePattern.SetValue, uiauto.uiauto_IUIAutomationValuePattern_SetValue, uiauto_IUIAutomationValuePattern_SetValue, uiautomationclient/IUIAutomationValuePattern::SetValue, winauto.uiauto_IUIAutomationValuePattern_SetValue
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
-	IUIAutomationValuePattern.SetValue
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationValuePattern::SetValue method


## -description


Sets the value of the element.


## -parameters




### -param val [in]

Type: <b>BSTR</b>

The value to set.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/65b1311d-479a-4be4-a9fb-7dfe885420b8">CurrentIsEnabled</a> property must be <b>TRUE</b>, and the <a href="https://msdn.microsoft.com/dc5111c4-6fc8-4a4f-b797-6da472fd0533">IUIAutomationValuePattern::CurrentIsReadOnly</a> property must be <b>FALSE</b>.
			



