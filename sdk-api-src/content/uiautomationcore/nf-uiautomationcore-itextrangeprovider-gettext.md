---
UID: NF:uiautomationcore.ITextRangeProvider.GetText
title: ITextRangeProvider::GetText (uiautomationcore.h)
description: Retrieves the plain text of the range.
helpviewer_keywords: ["GetText","GetText method [Windows Accessibility]","GetText method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","GetText method","ITextRangeProvider.GetText","ITextRangeProvider::GetText","uiauto.uiauto_ITextRangeProvider_GetText","uiauto_ITextRangeProvider_GetText","uiautomationcore/ITextRangeProvider::GetText","winauto.uiauto_ITextRangeProvider_GetText"]
old-location: winauto\uiauto_ITextRangeProvider_GetText.htm
tech.root: WinAuto
ms.assetid: f3c5f0cc-15a5-4a13-b3be-355de6633c66
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Windows Accessibility], GetText method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetText method, ITextRangeProvider.GetText, ITextRangeProvider::GetText, uiauto.uiauto_ITextRangeProvider_GetText, uiauto_ITextRangeProvider_GetText, uiautomationcore/ITextRangeProvider::GetText, winauto.uiauto_ITextRangeProvider_GetText
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
 - ITextRangeProvider::GetText
 - uiautomationcore/ITextRangeProvider::GetText
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
 - ITextRangeProvider.GetText
---

# ITextRangeProvider::GetText


## -description

Retrieves the plain text of the range.

## -parameters

### -param maxLength [in]

Type: <b>int</b>

The maximum length of the string to return. Use -1 if no limit is required.

### -param pRetVal [out, retval]

Type: <b>BSTR*</b>

Receives the plain text of the text range, 
				possibly truncated at the specified maximum length. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ITextRangeProvider::GetText</b> retrieves both hidden and visible text.

If <i>maxLength</i> is greater 
            than the length of the text span of the caller, the string returned will be the 
			plain text of the text range.

<b>ITextRangeProvider::GetText</b> will not be affected by the order of endpoints in the text flow; 
			it will always return the text between the start and end endpoints of the text range in the logical text flow order.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>