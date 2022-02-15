---
UID: NF:uiautomationclient.IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection
title: IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection (uiautomationclient.h)
description: Retrieves the Microsoft Active Accessibility property that identifies the selected children of this element.
helpviewer_keywords: ["GetCurrentSelection","GetCurrentSelection method [Windows Accessibility]","GetCurrentSelection method [Windows Accessibility]","IUIAutomationLegacyIAccessiblePattern interface","IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility]","GetCurrentSelection method","IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection","IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection","uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection","uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection","uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection","winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection"]
old-location: winauto\uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection.htm
tech.root: WinAuto
ms.assetid: 7fe666dc-2168-44a0-87f2-f444fd2a70f2
ms.date: 12/05/2018
ms.keywords: GetCurrentSelection, GetCurrentSelection method [Windows Accessibility], GetCurrentSelection method [Windows Accessibility],IUIAutomationLegacyIAccessiblePattern interface, IUIAutomationLegacyIAccessiblePattern interface [Windows Accessibility],GetCurrentSelection method, IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection, IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection, uiauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection, uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection, uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection, winauto.uiauto_IUIAutomationLegacyIAccessiblePattern_GetCurrentSelection
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection
 - uiautomationclient/IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection
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
 - IUIAutomationLegacyIAccessiblePattern.GetCurrentSelection
---

# IUIAutomationLegacyIAccessiblePattern::GetCurrentSelection


## -description

Retrieves the Microsoft Active Accessibility property that identifies the selected children of this element.

## -parameters

### -param pvarSelectedChildren [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelementarray">IUIAutomationElementArray</a>**</b>

Receives a pointer to the collection of the selected child elements.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationlegacyiaccessiblepattern">IUIAutomationLegacyIAccessiblePattern</a>