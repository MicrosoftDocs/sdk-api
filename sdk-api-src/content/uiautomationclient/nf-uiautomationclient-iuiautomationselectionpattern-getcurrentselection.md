---
UID: NF:uiautomationclient.IUIAutomationSelectionPattern.GetCurrentSelection
title: IUIAutomationSelectionPattern::GetCurrentSelection (uiautomationclient.h)

description: Retrieves the selected elements in the container.
old-location: winauto\uiauto_IUIAutomationSelectionPattern_GetCurrentSelection.htm
tech.root: WinAuto
ms.assetid: 58540e08-4415-47d1-8957-1d1c8b6d7100

ms.date: 12/05/2018
ms.keywords: GetCurrentSelection, GetCurrentSelection method [Windows Accessibility], GetCurrentSelection method [Windows Accessibility],IUIAutomationSelectionPattern interface, IUIAutomationSelectionPattern interface [Windows Accessibility],GetCurrentSelection method, IUIAutomationSelectionPattern.GetCurrentSelection, IUIAutomationSelectionPattern::GetCurrentSelection, uiauto.uiauto_IUIAutomationSelectionPattern_GetCurrentSelection, uiauto_IUIAutomationSelectionPattern_GetCurrentSelection, uiautomationclient/IUIAutomationSelectionPattern::GetCurrentSelection, winauto.uiauto_IUIAutomationSelectionPattern_GetCurrentSelection
ms.topic: method
f1_keywords: 
 - "uiautomationclient/IUIAutomationSelectionPattern.GetCurrentSelection"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationSelectionPattern.GetCurrentSelection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationSelectionPattern::GetCurrentSelection


## -description


Retrieves the selected elements in the container.


## -parameters




### -param retVal [out, retval]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of selected elements. The default is an empty array.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationselectionpattern">IUIAutomationSelectionPattern</a>
 

 

