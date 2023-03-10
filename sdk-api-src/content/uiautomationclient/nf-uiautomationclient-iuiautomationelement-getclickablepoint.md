---
UID: NF:uiautomationclient.IUIAutomationElement.GetClickablePoint
title: IUIAutomationElement::GetClickablePoint (uiautomationclient.h)
description: Retrieves a point on the element that can be clicked.
helpviewer_keywords: ["GetClickablePoint","GetClickablePoint method [Windows Accessibility]","GetClickablePoint method [Windows Accessibility]","IUIAutomationElement interface","IUIAutomationElement interface [Windows Accessibility]","GetClickablePoint method","IUIAutomationElement.GetClickablePoint","IUIAutomationElement::GetClickablePoint","uiauto.uiauto_IUIAutomationElement_GetClickablePoint","uiauto_IUIAutomationElement_GetClickablePoint","uiautomationclient/IUIAutomationElement::GetClickablePoint","winauto.uiauto_IUIAutomationElement_GetClickablePoint"]
old-location: winauto\uiauto_IUIAutomationElement_GetClickablePoint.htm
tech.root: WinAuto
ms.assetid: 3762aac6-5bd8-43a6-8fe6-e79d8724622b
ms.date: 12/05/2018
ms.keywords: GetClickablePoint, GetClickablePoint method [Windows Accessibility], GetClickablePoint method [Windows Accessibility],IUIAutomationElement interface, IUIAutomationElement interface [Windows Accessibility],GetClickablePoint method, IUIAutomationElement.GetClickablePoint, IUIAutomationElement::GetClickablePoint, uiauto.uiauto_IUIAutomationElement_GetClickablePoint, uiauto_IUIAutomationElement_GetClickablePoint, uiautomationclient/IUIAutomationElement::GetClickablePoint, winauto.uiauto_IUIAutomationElement_GetClickablePoint
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
 - IUIAutomationElement::GetClickablePoint
 - uiautomationclient/IUIAutomationElement::GetClickablePoint
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
 - IUIAutomationElement.GetClickablePoint
---

# IUIAutomationElement::GetClickablePoint


## -description

Retrieves a point on the element that can be clicked.

## -parameters

### -param clickable [out]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

Receives the physical screen coordinates of a point that can be used by a client to click this element.

### -param gotClickable [out, retval]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a>*</b>

Receives <b>TRUE</b> if a clickable point was retrieved, or <b>FALSE</b> otherwise.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A client application can use this method to simulate clicking the left or right mouse button. For example, to simulate clicking the right mouse button to display the context menu for a control: 

<ul>
<li>Call the <b>GetClickablePoint</b> method to find a clickable point on the control.</li>
<li>Call the <a href="/windows/desktop/api/winuser/nf-winuser-sendinput">SendInput</a> function to send a right-mouse-down, right-mouse-up sequence.</li>
</ul>

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">Automation Element Property IDs</a>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>



<b>Reference</b>