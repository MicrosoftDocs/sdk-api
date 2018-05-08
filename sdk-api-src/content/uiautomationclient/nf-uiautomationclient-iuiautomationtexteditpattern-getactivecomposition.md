---
UID: NF:uiautomationclient.IUIAutomationTextEditPattern.GetActiveComposition
title: IUIAutomationTextEditPattern::GetActiveComposition
author: windows-driver-content
description: Returns the active composition.
old-location: winauto\uiauto_IUIAutomationTextEditPattern_GetActiveComposition.htm
old-project: WinAuto
ms.assetid: F6503B77-19FB-6D00-D20C-E3D3F0EC28DA
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetActiveComposition, GetActiveComposition method [Windows Accessibility], GetActiveComposition method [Windows Accessibility],IUIAutomationTextEditPattern interface, IUIAutomationTextEditPattern interface [Windows Accessibility],GetActiveComposition method, IUIAutomationTextEditPattern.GetActiveComposition, IUIAutomationTextEditPattern::GetActiveComposition, uiautomationclient/IUIAutomationTextEditPattern::GetActiveComposition, winauto.uiauto_IUIAutomationTextEditPattern_GetActiveComposition
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
-	IUIAutomationTextEditPattern.GetActiveComposition
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextEditPattern::GetActiveComposition


## -description


Returns the active composition.


## -parameters




### -param range [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Pointer to the range of the current conversion (none if there is no conversion).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Active composition is relevant to Input Method Editors (IMEs).




## -see-also




<a href="https://msdn.microsoft.com/798FABE5-D6C8-58E3-B3F6-93654C0F4CAB">IUIAutomationTextEditPattern</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

