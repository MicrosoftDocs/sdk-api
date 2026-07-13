---
UID: NF:uiautomationclient.IUIAutomationTextRange.GetBoundingRectangles
title: IUIAutomationTextRange::GetBoundingRectangles (uiautomationclient.h)
description: Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range. (IUIAutomationTextRange.GetBoundingRectangles)
helpviewer_keywords: ["GetBoundingRectangles","GetBoundingRectangles method [Windows Accessibility]","GetBoundingRectangles method [Windows Accessibility]","IUIAutomationTextRange interface","IUIAutomationTextRange interface [Windows Accessibility]","GetBoundingRectangles method","IUIAutomationTextRange.GetBoundingRectangles","IUIAutomationTextRange::GetBoundingRectangles","uiauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles","uiauto_IUIAutomationTextRange_GetBoundingRectangles","uiautomationclient/IUIAutomationTextRange::GetBoundingRectangles","winauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles"]
old-location: winauto\uiauto_IUIAutomationTextRange_GetBoundingRectangles.htm
tech.root: WinAuto
ms.assetid: a155d143-c5ec-4669-9635-fb8f8012a684
ms.date: 12/05/2018
ms.keywords: GetBoundingRectangles, GetBoundingRectangles method [Windows Accessibility], GetBoundingRectangles method [Windows Accessibility],IUIAutomationTextRange interface, IUIAutomationTextRange interface [Windows Accessibility],GetBoundingRectangles method, IUIAutomationTextRange.GetBoundingRectangles, IUIAutomationTextRange::GetBoundingRectangles, uiauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles, uiauto_IUIAutomationTextRange_GetBoundingRectangles, uiautomationclient/IUIAutomationTextRange::GetBoundingRectangles, winauto.uiauto_IUIAutomationTextRange_GetBoundingRectangles
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
 - IUIAutomationTextRange::GetBoundingRectangles
 - uiautomationclient/IUIAutomationTextRange::GetBoundingRectangles
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
 - IUIAutomationTextRange.GetBoundingRectangles
---

# IUIAutomationTextRange::GetBoundingRectangles


## -description

Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.

## -parameters

### -param boundingRects [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to an array of bounding rectangles for each fully or partially visible line of text in a text range. An empty array is returned for a degenerate (empty) text range or for a text range that is  completely off-screen, scrolled out of view, or obscured by an overlapping window.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For information about how the bounding rectangles are stored in the SAFEARRAY, see <a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationtextrange">IUIAutomationTextRange</a>



<b>Reference</b>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-safearraytorectnativearray">SafeArrayToRectNativeArray</a>



<a href="/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
