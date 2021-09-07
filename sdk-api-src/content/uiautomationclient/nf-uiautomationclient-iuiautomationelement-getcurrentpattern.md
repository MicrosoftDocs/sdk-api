---
UID: NF:uiautomationclient.IUIAutomationElement.GetCurrentPattern
title: IUIAutomationElement::GetCurrentPattern (uiautomationclient.h)
description: Retrieves the IUnknown interface of the specified control pattern on this UI Automation element.
helpviewer_keywords: ["GetCurrentPattern","GetCurrentPattern method [Windows Accessibility]","GetCurrentPattern method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetCurrentPattern method","IUIAutomationElement.GetCurrentPattern","IUIAutomationElement::GetCurrentPattern","uiauto.uiauto_IUIAutomationElement_GetCurrentPattern","uiauto_IUIAutomationElement_GetCurrentPattern","uiautomationclient/IUIAutomationElement::GetCurrentPattern","winauto.uiauto_IUIAutomationElement_GetCurrentPattern"]
old-location: winauto\uiauto_IUIAutomationElement_GetCurrentPattern.htm
tech.root: WinAuto
ms.assetid: 3ad4df7c-979d-464f-9600-d1f3de064b59
ms.date: 12/05/2018
ms.keywords: GetCurrentPattern, GetCurrentPattern method [Windows Accessibility], GetCurrentPattern method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCurrentPattern method, IUIAutomationElement.GetCurrentPattern, IUIAutomationElement::GetCurrentPattern, uiauto.uiauto_IUIAutomationElement_GetCurrentPattern, uiauto_IUIAutomationElement_GetCurrentPattern, uiautomationclient/IUIAutomationElement::GetCurrentPattern, winauto.uiauto_IUIAutomationElement_GetCurrentPattern
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
 - IUIAutomationElement::GetCurrentPattern
 - uiautomationclient/IUIAutomationElement::GetCurrentPattern
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
 - IUIAutomationElement.GetCurrentPattern
---

# IUIAutomationElement::GetCurrentPattern


## -description

Retrieves the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the specified control pattern on this UI Automation element.

## -parameters

### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

### -param patternObject [out, retval]

Type: <b><a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>**</b>

Receives a pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method gets the specified control pattern based on its availability at the time of the call.

For some forms of UI, this method will incur cross-process performance overhead. Applications can reduce overhead by caching control patterns and then retrieving them by using <a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpattern">IUIAutomationElement::GetCachedPattern</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpattern">GetCachedPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpatternas">GetCurrentPatternAs</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-controlpatternsoverview">UI Automation Control Patterns Overview</a>