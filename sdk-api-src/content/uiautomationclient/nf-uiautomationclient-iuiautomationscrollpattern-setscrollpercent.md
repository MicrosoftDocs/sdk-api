---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.SetScrollPercent
title: IUIAutomationScrollPattern::SetScrollPercent (uiautomationclient.h)
description: Sets the horizontal and vertical scroll positions as a percentage of the total content area within the UI Automation element.
helpviewer_keywords: ["IUIAutomationScrollPattern interface [Windows Accessibility]","SetScrollPercent method","IUIAutomationScrollPattern.SetScrollPercent","IUIAutomationScrollPattern::SetScrollPercent","SetScrollPercent","SetScrollPercent method [Windows Accessibility]","SetScrollPercent method [Windows Accessibility]","IUIAutomationScrollPattern interface","uiauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent","uiauto_IUIAutomationScrollPattern_SetScrollPercent","uiautomationclient/IUIAutomationScrollPattern::SetScrollPercent","winauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent"]
old-location: winauto\uiauto_IUIAutomationScrollPattern_SetScrollPercent.htm
tech.root: WinAuto
ms.assetid: 2f31445d-6198-430a-8f31-3ff25b72581c
ms.date: 12/05/2018
ms.keywords: IUIAutomationScrollPattern interface [Windows Accessibility],SetScrollPercent method, IUIAutomationScrollPattern.SetScrollPercent, IUIAutomationScrollPattern::SetScrollPercent, SetScrollPercent, SetScrollPercent method [Windows Accessibility], SetScrollPercent method [Windows Accessibility],IUIAutomationScrollPattern interface, uiauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent, uiauto_IUIAutomationScrollPattern_SetScrollPercent, uiautomationclient/IUIAutomationScrollPattern::SetScrollPercent, winauto.uiauto_IUIAutomationScrollPattern_SetScrollPercent
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
 - IUIAutomationScrollPattern::SetScrollPercent
 - uiautomationclient/IUIAutomationScrollPattern::SetScrollPercent
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
 - IUIAutomationScrollPattern.SetScrollPercent
---

# IUIAutomationScrollPattern::SetScrollPercent


## -description

Sets the horizontal and vertical scroll positions as a percentage of the total content area within the UI Automation element.

## -parameters

### -param horizontalPercent [in]

Type: <b>double</b>

The percentage of the total horizontal content area, or <b>UIA_ScrollPatternNoScroll</b> if the horizontal position is not to be set.

### -param verticalPercent [in]

Type: <b>double</b>

The percentage of the total vertical content area, or <b>UIA_ScrollPatternNoScroll</b> if the vertical position is not to be set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is useful only when the content area of the control is larger than the visible region.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationscrollpattern">IUIAutomationScrollPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationscrollpattern-scroll">IUIAutomationScrollPattern::Scroll</a>