---
UID: NF:uiautomationclient.IUIAutomationSelectionItemPattern.RemoveFromSelection
title: IUIAutomationSelectionItemPattern::RemoveFromSelection (uiautomationclient.h)
description: Removes this element from the selection.
helpviewer_keywords: ["IUIAutomationSelectionItemPattern interface [Windows Accessibility]","RemoveFromSelection method","IUIAutomationSelectionItemPattern.RemoveFromSelection","IUIAutomationSelectionItemPattern::RemoveFromSelection","RemoveFromSelection","RemoveFromSelection method [Windows Accessibility]","RemoveFromSelection method [Windows Accessibility]","IUIAutomationSelectionItemPattern interface","uiauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection","uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection","uiautomationclient/IUIAutomationSelectionItemPattern::RemoveFromSelection","winauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection"]
old-location: winauto\uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection.htm
tech.root: WinAuto
ms.assetid: 25f9a8da-4bc9-496e-888c-a270a2bf8fb3
ms.date: 12/05/2018
ms.keywords: IUIAutomationSelectionItemPattern interface [Windows Accessibility],RemoveFromSelection method, IUIAutomationSelectionItemPattern.RemoveFromSelection, IUIAutomationSelectionItemPattern::RemoveFromSelection, RemoveFromSelection, RemoveFromSelection method [Windows Accessibility], RemoveFromSelection method [Windows Accessibility],IUIAutomationSelectionItemPattern interface, uiauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection, uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection, uiautomationclient/IUIAutomationSelectionItemPattern::RemoveFromSelection, winauto.uiauto_IUIAutomationSelectionItemPattern_RemoveFromSelection
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUIAutomationSelectionItemPattern::RemoveFromSelection
 - uiautomationclient/IUIAutomationSelectionItemPattern::RemoveFromSelection
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationSelectionItemPattern.RemoveFromSelection
---

# IUIAutomationSelectionItemPattern::RemoveFromSelection


## -description

Removes this element from the selection.



## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

An error code is returned if this element is the only one in the selection and the selection container requires at least one element to be selected.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection">AddToSelection</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionpattern-get_currentisselectionrequired">CurrentIsSelectionRequired</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionitempattern">IUIAutomationSelectionItemPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationselectionitempattern-select">Select</a>
