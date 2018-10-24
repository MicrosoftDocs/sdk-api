---
UID: NF:uiautomationcore.ITextRangeProvider.AddToSelection
title: ITextRangeProvider::AddToSelection
author: windows-sdk-content
description: Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.
old-location: winauto\uiauto_ITextRangeProvider_AddToSelection.htm
tech.root: WinAuto
ms.assetid: e058ca62-6bb4-403e-a355-cc422a329109
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: AddToSelection, AddToSelection method [Windows Accessibility], AddToSelection method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],AddToSelection method, ITextRangeProvider.AddToSelection, ITextRangeProvider::AddToSelection, uiauto.uiauto_ITextRangeProvider_AddToSelection, uiauto_ITextRangeProvider_AddToSelection, uiautomationcore/ITextRangeProvider::AddToSelection, winauto.uiauto_ITextRangeProvider_AddToSelection
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
 - ITextRangeProvider.AddToSelection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::AddToSelection


## -description


Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.


## -parameters






## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text insertion point moves to the area of the new selection.
            

If this method is called on a degenerate text range, the text insertion point moves to the location of the text range but no text is selected. 
            




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

