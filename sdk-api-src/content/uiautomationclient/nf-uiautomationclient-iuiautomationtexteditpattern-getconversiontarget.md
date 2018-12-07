---
UID: NF:uiautomationclient.IUIAutomationTextEditPattern.GetConversionTarget
title: IUIAutomationTextEditPattern::GetConversionTarget
author: windows-sdk-content
description: Returns the current conversion target range.
old-location: winauto\uiauto_IUIAutomationTextEditPattern_GetConversionTarget.htm
tech.root: WinAuto
ms.assetid: C7471306-9D7F-5FE8-9A57-7A3ABB45B59F
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetConversionTarget, GetConversionTarget method [Windows Accessibility], GetConversionTarget method [Windows Accessibility],IUIAutomationTextEditPattern interface, IUIAutomationTextEditPattern interface [Windows Accessibility],GetConversionTarget method, IUIAutomationTextEditPattern.GetConversionTarget, IUIAutomationTextEditPattern::GetConversionTarget, uiautomationclient/IUIAutomationTextEditPattern::GetConversionTarget, winauto.uiauto_IUIAutomationTextEditPattern_GetConversionTarget
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
 - IUIAutomationTextEditPattern.GetConversionTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationTextEditPattern::GetConversionTarget


## -description


Returns the current conversion target range.


## -parameters




### -param range [out, retval]

Type: <b><a href="https://msdn.microsoft.com/1037919d-c8df-4d46-b3ce-62ee23c92145">IUIAutomationTextRange</a>**</b>

Pointer to the conversion target range (none if there is no conversion).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/798FABE5-D6C8-58E3-B3F6-93654C0F4CAB">IUIAutomationTextEditPattern</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

