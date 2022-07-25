---
UID: NF:uiautomationcore.ITextRangeProvider.FindText
title: ITextRangeProvider::FindText (uiautomationcore.h)
description: Returns a text range subset that contains the specified text.
helpviewer_keywords: ["FindText","FindText method [Windows Accessibility]","FindText method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","FindText method","ITextRangeProvider.FindText","ITextRangeProvider::FindText","uiauto.uiauto_ITextRangeProvider_FindText","uiauto_ITextRangeProvider_FindText","uiautomationcore/ITextRangeProvider::FindText","winauto.uiauto_ITextRangeProvider_FindText"]
old-location: winauto\uiauto_ITextRangeProvider_FindText.htm
tech.root: WinAuto
ms.assetid: 6012bc1e-5c1c-4874-ba2b-5e16eaf21f1d
ms.date: 12/05/2018
ms.keywords: FindText, FindText method [Windows Accessibility], FindText method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],FindText method, ITextRangeProvider.FindText, ITextRangeProvider::FindText, uiauto.uiauto_ITextRangeProvider_FindText, uiauto_ITextRangeProvider_FindText, uiautomationcore/ITextRangeProvider::FindText, winauto.uiauto_ITextRangeProvider_FindText
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - ITextRangeProvider::FindText
 - uiautomationcore/ITextRangeProvider::FindText
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
 - ITextRangeProvider.FindText
---

# ITextRangeProvider::FindText


## -description

Returns a text range subset that contains the specified text.

## -parameters

### -param text [in]

Type: <b>BSTR</b>

The text string to search for.

### -param backward [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if the last occurring text range should be returned instead of the first; otherwise <b>FALSE</b>.

### -param ignoreCase [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

<b>TRUE</b> if case should be ignored; otherwise <b>FALSE</b>.

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>**</b>

Receives a pointer to the text range
				matching the specified text; otherwise <b>NULL</b>. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

There is no differentiation between hidden and visible text.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>