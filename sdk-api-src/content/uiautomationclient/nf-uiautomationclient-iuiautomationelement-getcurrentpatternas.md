---
UID: NF:uiautomationclient.IUIAutomationElement.GetCurrentPatternAs
title: IUIAutomationElement::GetCurrentPatternAs (uiautomationclient.h)
description: Retrieves the control pattern interface of the specified pattern on this UI Automation element.
helpviewer_keywords: ["GetCurrentPatternAs","GetCurrentPatternAs method [Windows Accessibility]","GetCurrentPatternAs method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetCurrentPatternAs method","IUIAutomationElement.GetCurrentPatternAs","IUIAutomationElement::GetCurrentPatternAs","uiauto.uiauto_IUIAutomationElement_GetCurrentPatternAs","uiauto_IUIAutomationElement_GetCurrentPatternAs","uiautomationclient/IUIAutomationElement::GetCurrentPatternAs","winauto.uiauto_IUIAutomationElement_GetCurrentPatternAs"]
old-location: winauto\uiauto_IUIAutomationElement_GetCurrentPatternAs.htm
tech.root: WinAuto
ms.assetid: 98b0f647-7f6e-4e07-8530-1dae781507bc
ms.date: 12/05/2018
ms.keywords: GetCurrentPatternAs, GetCurrentPatternAs method [Windows Accessibility], GetCurrentPatternAs method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetCurrentPatternAs method, IUIAutomationElement.GetCurrentPatternAs, IUIAutomationElement::GetCurrentPatternAs, uiauto.uiauto_IUIAutomationElement_GetCurrentPatternAs, uiauto_IUIAutomationElement_GetCurrentPatternAs, uiautomationclient/IUIAutomationElement::GetCurrentPatternAs, winauto.uiauto_IUIAutomationElement_GetCurrentPatternAs
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
 - IUIAutomationElement::GetCurrentPatternAs
 - uiautomationclient/IUIAutomationElement::GetCurrentPatternAs
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
 - IUIAutomationElement.GetCurrentPatternAs
---

# IUIAutomationElement::GetCurrentPatternAs


## -description

Retrieves the control pattern interface of the specified pattern on this UI Automation element.

## -parameters

### -param patternId [in]

Type: <b>PATTERNID</b>

The identifier of the control pattern. For a list of control pattern IDs, see <a href="/windows/desktop/WinAuto/uiauto-controlpattern-ids">Control Pattern Identifiers</a>.

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.

### -param patternObject [out]

Type: <b>void**</b>

Receives the interface pointer requested in <i>riid</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

It is recommended that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcachedpatternas">GetCachedPatternAs</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern">GetCurrentPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-controlpatternsoverview">UI Automation Control Patterns Overview</a>