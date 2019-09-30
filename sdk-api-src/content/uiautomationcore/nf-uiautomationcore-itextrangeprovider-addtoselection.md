---
UID: NF:uiautomationcore.ITextRangeProvider.AddToSelection
title: ITextRangeProvider::AddToSelection (uiautomationcore.h)
author: windows-sdk-content
description: Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.
old-location: winauto\uiauto_ITextRangeProvider_AddToSelection.htm
tech.root: WinAuto
ms.assetid: e058ca62-6bb4-403e-a355-cc422a329109
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AddToSelection, AddToSelection method [Windows Accessibility], AddToSelection method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],AddToSelection method, ITextRangeProvider.AddToSelection, ITextRangeProvider::AddToSelection, uiauto.uiauto_ITextRangeProvider_AddToSelection, uiauto_ITextRangeProvider_AddToSelection, uiautomationcore/ITextRangeProvider::AddToSelection, winauto.uiauto_ITextRangeProvider_AddToSelection
ms.topic: method
f1_keywords: 
 - "uiautomationcore/ITextRangeProvider.AddToSelection"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextRangeProvider::AddToSelection


## -description


Adds the text range to the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The text insertion point moves to the area of the new selection.
            

If this method is called on a degenerate text range, the text insertion point moves to the location of the text range but no text is selected. 
            




## -see-also




<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

