---
UID: NF:uiautomationclient.IUIAutomationScrollPattern.Scroll
title: IUIAutomationScrollPattern::Scroll (uiautomationclient.h)
description: Scrolls the visible region of the content area horizontally and vertically. (IUIAutomationScrollPattern.Scroll)
helpviewer_keywords: ["IUIAutomationScrollPattern interface [Windows Accessibility]","Scroll method","IUIAutomationScrollPattern.Scroll","IUIAutomationScrollPattern::Scroll","Scroll","Scroll method [Windows Accessibility]","Scroll method [Windows Accessibility]","IUIAutomationScrollPattern interface","uiauto.uiauto_IUIAutomationScrollPattern_Scroll","uiauto_IUIAutomationScrollPattern_Scroll","uiautomationclient/IUIAutomationScrollPattern::Scroll","winauto.uiauto_IUIAutomationScrollPattern_Scroll"]
old-location: winauto\uiauto_IUIAutomationScrollPattern_Scroll.htm
tech.root: WinAuto
ms.assetid: 2deb7399-604d-45eb-95d6-f1135550a18f
ms.date: 12/05/2018
ms.keywords: IUIAutomationScrollPattern interface [Windows Accessibility],Scroll method, IUIAutomationScrollPattern.Scroll, IUIAutomationScrollPattern::Scroll, Scroll, Scroll method [Windows Accessibility], Scroll method [Windows Accessibility],IUIAutomationScrollPattern interface, uiauto.uiauto_IUIAutomationScrollPattern_Scroll, uiauto_IUIAutomationScrollPattern_Scroll, uiautomationclient/IUIAutomationScrollPattern::Scroll, winauto.uiauto_IUIAutomationScrollPattern_Scroll
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
 - IUIAutomationScrollPattern::Scroll
 - uiautomationclient/IUIAutomationScrollPattern::Scroll
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
 - IUIAutomationScrollPattern.Scroll
---

# IUIAutomationScrollPattern::Scroll


## -description

Scrolls the visible region of the content area horizontally and vertically.

## -parameters

### -param horizontalAmount [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

A value indicating the size of the horizontal scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the horizontal position is not to be set.

### -param verticalAmount [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-scrollamount">ScrollAmount</a> enumerated type indicating the size of the vertical scroll increment, or <b>UIA_ScrollPatternNoScroll</b> if the vertical position is not to be set.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationscrollpattern">IUIAutomationScrollPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationscrollpattern-setscrollpercent">IUIAutomationScrollPattern::SetScrollPercent</a>
