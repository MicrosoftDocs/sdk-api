---
UID: NF:uiautomationcore.ITextProvider.GetSelection
title: ITextProvider::GetSelection (uiautomationcore.h)
description: Retrieves a collection of text ranges that represents the currently selected text in a text-based control. (ITextProvider.GetSelection)
helpviewer_keywords: ["GetSelection","GetSelection method [Windows Accessibility]","GetSelection method [Windows Accessibility]","ITextProvider interface","ITextProvider interface [Windows Accessibility]","GetSelection method","ITextProvider.GetSelection","ITextProvider::GetSelection","uiauto.uiauto_ITextProvider_GetSelection","uiauto_ITextProvider_GetSelection","uiautomationcore/ITextProvider::GetSelection","winauto.uiauto_ITextProvider_GetSelection"]
old-location: winauto\uiauto_ITextProvider_GetSelection.htm
tech.root: WinAuto
ms.assetid: f5c0b2ed-e891-4856-8829-617a69d4708a
ms.date: 12/05/2018
ms.keywords: GetSelection, GetSelection method [Windows Accessibility], GetSelection method [Windows Accessibility],ITextProvider interface, ITextProvider interface [Windows Accessibility],GetSelection method, ITextProvider.GetSelection, ITextProvider::GetSelection, uiauto.uiauto_ITextProvider_GetSelection, uiauto_ITextProvider_GetSelection, uiautomationcore/ITextProvider::GetSelection, winauto.uiauto_ITextProvider_GetSelection
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
 - ITextProvider::GetSelection
 - uiautomationcore/ITextProvider::GetSelection
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
 - ITextProvider.GetSelection
---

# ITextProvider::GetSelection


## -description

Retrieves a collection of text ranges that represents the currently selected text in a text-based control.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives the address of an array of pointers to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a> interfaces of the text ranges,
				one for each selected span of text. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For UI Automation providers that support text selection, 
        the provider should implement this method and also return a <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider-get_supportedtextselection">ITextProvider::SupportedTextSelection</a> value.
        

If the control contains only a single span of selected text, the <i>pRetVal</i> array should contain a single text range. 

If the control contains a text insertion point but no text is selected,  the <i>pRetVal</i> array should contain a degenerate (empty) text range at the position of the text insertion point.

 If the control contains no selected text, or if the control does not contain a text insertion point, set <i>pRetVal</i> to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
