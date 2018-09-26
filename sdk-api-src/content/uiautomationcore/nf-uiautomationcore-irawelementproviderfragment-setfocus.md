---
UID: NF:uiautomationcore.IRawElementProviderFragment.SetFocus
title: IRawElementProviderFragment::SetFocus
author: windows-sdk-content
description: Sets the focus to this element.
old-location: winauto\uiauto_IRawElementProviderFragment_SetFocus.htm
tech.root: WinAuto
ms.assetid: 343959bc-42d0-4289-b507-7da78cee28f2
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: IRawElementProviderFragment interface [Windows Accessibility],SetFocus method, IRawElementProviderFragment.SetFocus, IRawElementProviderFragment::SetFocus, SetFocus, SetFocus method [Windows Accessibility], SetFocus method [Windows Accessibility],IRawElementProviderFragment interface, uiauto.uiauto_IRawElementProviderFragment_SetFocus, uiauto_IRawElementProviderFragment_SetFocus, uiautomationcore/IRawElementProviderFragment::SetFocus, winauto.uiauto_IRawElementProviderFragment_SetFocus
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderFragment.SetFocus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderFragment::SetFocus


## -description


Sets the focus to this element.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The Microsoft UI Automation framework will ensure that the part of the interface that hosts this fragment is 
			already focused before calling this method. Your implementation should update only its internal focus state; 
			for example, by repainting a list item to show that it has the focus. If you prefer that UI Automation 
			not focus the parent window, set <a href="uiauto_ProvOptionsEnum.htm">ProviderOptions_ProviderOwnsSetFocus</a> in <a href="https://msdn.microsoft.com/fd41bb43-bbf1-4022-9472-0ad2816074c6">IRawElementProviderSimple::ProviderOptions</a> for the fragment root.





## -see-also




<a href="https://msdn.microsoft.com/63539ba9-7f13-48cf-9c8a-74c03d31e2ab">IRawElementProviderFragment</a>
 

 

