---
UID: NF:uiautomationcore.ITextRangeProvider.RemoveFromSelection
title: ITextRangeProvider::RemoveFromSelection (uiautomationcore.h)
description: Removes the text range from the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","RemoveFromSelection method","ITextRangeProvider.RemoveFromSelection","ITextRangeProvider::RemoveFromSelection","RemoveFromSelection","RemoveFromSelection method [Windows Accessibility]","RemoveFromSelection method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_RemoveFromSelection","uiauto_ITextRangeProvider_RemoveFromSelection","uiautomationcore/ITextRangeProvider::RemoveFromSelection","winauto.uiauto_ITextRangeProvider_RemoveFromSelection"]
old-location: winauto\uiauto_ITextRangeProvider_RemoveFromSelection.htm
tech.root: WinAuto
ms.assetid: 057d784e-906a-4de8-bdd8-b58a2e26f37c
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],RemoveFromSelection method, ITextRangeProvider.RemoveFromSelection, ITextRangeProvider::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_RemoveFromSelection, uiauto_ITextRangeProvider_RemoveFromSelection, uiautomationcore/ITextRangeProvider::RemoveFromSelection, winauto.uiauto_ITextRangeProvider_RemoveFromSelection
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITextRangeProvider::RemoveFromSelection
 - uiautomationcore/ITextRangeProvider::RemoveFromSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.RemoveFromSelection
---

# ITextRangeProvider::RemoveFromSelection


## -description

Removes the text range from the collection of selected text ranges in a control that supports multiple, disjoint spans of selected text.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The text insertion point moves to the area of the removed selection.
            

If this method is called on a degenerate text range, the text insertion point moves to the location of the text range but no text is selected.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
