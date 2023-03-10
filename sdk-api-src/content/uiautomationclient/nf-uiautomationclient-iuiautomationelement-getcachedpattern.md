---
UID: NF:uiautomationclient.IUIAutomationElement.GetCachedPattern
title: IUIAutomationElement::GetCachedPattern (uiautomationclient.h)
description: Retrieves from the cache the IUnknown interface of the specified control pattern of this UI Automation element.
helpviewer_keywords: ["GetCachedPattern","GetCachedPattern method [Windows Accessibility]","GetCachedPattern method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetCachedPattern method","IUIAutomationElement.GetCachedPattern","IUIAutomationElement::GetCachedPattern","uiauto.uiauto_IUIAutomationElement_GetCachedPattern","uiauto_IUIAutomationElement_GetCachedPattern","uiautomationclient/IUIAutomationElement::GetCachedPattern","winauto.uiauto_IUIAutomationElement_GetCachedPattern"]
old-location: winauto\uiauto_IUIAutomationElement_GetCachedPattern.htm
tech.root: WinAuto
ms.assetid: c71cab11-24c7-4e66-bcf2-f1abb1f37abb
ms.date: 12/05/2018
ms.keywords: GetCachedPattern, GetCachedPattern method [Windows Accessibility], GetCachedPattern method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCachedPattern method, IUIAutomationElement.GetCachedPattern, IUIAutomationElement::GetCachedPattern, uiauto.uiauto_IUIAutomationElement_GetCachedPattern, uiauto_IUIAutomationElement_GetCachedPattern, uiautomationclient/IUIAutomationElement::GetCachedPattern, winauto.uiauto_IUIAutomationElement_GetCachedPattern
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
 - IUIAutomationElement::GetCachedPattern
 - uiautomationclient/IUIAutomationElement::GetCachedPattern
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
 - IUIAutomationElement.GetCachedPattern
---

# IUIAutomationElement::GetCachedPattern


## -description

Retrieves from the cache the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the specified control pattern of this UI Automation element.

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

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas">GetCachedPatternAs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern">GetCurrentPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-controlpatternsoverview">UI Automation Control Patterns Overview</a>