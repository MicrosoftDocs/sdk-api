---
UID: NF:uiautomationcore.ITextProvider2.GetCaretRange
title: ITextProvider2::GetCaretRange (uiautomationcore.h)
description: Provides a zero-length text range at the location of the caret that belongs to the text-based control.
helpviewer_keywords: ["GetCaretRange","GetCaretRange method [Windows Accessibility]","GetCaretRange method [Windows Accessibility]","ITextProvider2 interface","ITextProvider2 interface [Windows Accessibility]","GetCaretRange method","ITextProvider2.GetCaretRange","ITextProvider2::GetCaretRange","uiautomationcore/ITextProvider2::GetCaretRange","winauto.uiauto_ITextProvider2_GetCaretRange"]
old-location: winauto\uiauto_ITextProvider2_GetCaretRange.htm
tech.root: WinAuto
ms.assetid: 9DD77361-25E8-40A3-BDF4-AFE06F9D36F4
ms.date: 12/05/2018
ms.keywords: GetCaretRange, GetCaretRange method [Windows Accessibility], GetCaretRange method [Windows Accessibility],ITextProvider2 interface, ITextProvider2 interface [Windows Accessibility],GetCaretRange method, ITextProvider2.GetCaretRange, ITextProvider2::GetCaretRange, uiautomationcore/ITextProvider2::GetCaretRange, winauto.uiauto_ITextProvider2_GetCaretRange
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - ITextProvider2::GetCaretRange
 - uiautomationcore/ITextProvider2::GetCaretRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextProvider2.GetCaretRange
---

# ITextProvider2::GetCaretRange


## -description

Provides a zero-length text range at the location of the caret that belongs to the text-based control.

## -parameters

### -param isActive [out]

Type: <b>BOOL*</b>

<b>TRUE</b> if the text-based control that contains the caret has keyboard focus, otherwise <b>FALSE</b>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

 A text range that represents the current location of the caret that belongs to the text-based control.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the <i>isActive</i> parameter is <b>FALSE</b>, the caret that belongs to the text-based control might not be at the same location as the system caret.

This method retrieves a text range that a client can use to find the bounding rectangle of the caret that belongs to the text-based control, or to find the text near the caret.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider2">ITextProvider2</a>