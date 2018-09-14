---
UID: NF:uiautomationcore.ITextRangeProvider.Select
title: ITextRangeProvider::Select
author: windows-sdk-content
description: Selects the span of text that corresponds to this text range, and removes any previous selection.
old-location: winauto\uiauto_ITextRangeProvider_Select.htm
tech.root: WinAuto
ms.assetid: 486a604f-cea7-48de-aca2-2e9355699845
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],Select method, ITextRangeProvider.Select, ITextRangeProvider::Select, Select, Select method [Windows Accessibility], Select method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_Select, uiauto_ITextRangeProvider_Select, uiautomationcore/ITextRangeProvider::Select, winauto.uiauto_ITextRangeProvider_Select
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
 - ITextRangeProvider.Select
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::Select


## -description


Selects the span of text that corresponds to this text range, and removes any previous  selection. 


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Providing a degenerate text range will move the text insertion point. 
            




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

