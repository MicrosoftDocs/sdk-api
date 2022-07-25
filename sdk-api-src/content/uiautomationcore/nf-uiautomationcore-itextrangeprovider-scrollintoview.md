---
UID: NF:uiautomationcore.ITextRangeProvider.ScrollIntoView
title: ITextRangeProvider::ScrollIntoView (uiautomationcore.h)
description: Causes the text control to scroll vertically until the text range is visible in the viewport.
helpviewer_keywords: ["ITextRangeProvider interface [Windows Accessibility]","ScrollIntoView method","ITextRangeProvider.ScrollIntoView","ITextRangeProvider::ScrollIntoView","ScrollIntoView","ScrollIntoView method [Windows Accessibility]","ScrollIntoView method [Windows Accessibility]","ITextRangeProvider interface","uiauto.uiauto_ITextRangeProvider_ScrollIntoView","uiauto_ITextRangeProvider_ScrollIntoView","uiautomationcore/ITextRangeProvider::ScrollIntoView","winauto.uiauto_ITextRangeProvider_ScrollIntoView"]
old-location: winauto\uiauto_ITextRangeProvider_ScrollIntoView.htm
tech.root: WinAuto
ms.assetid: 58044de0-124f-4efd-a14f-4865f3278421
ms.date: 12/05/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],ScrollIntoView method, ITextRangeProvider.ScrollIntoView, ITextRangeProvider::ScrollIntoView, ScrollIntoView, ScrollIntoView method [Windows Accessibility], ScrollIntoView method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_ScrollIntoView, uiauto_ITextRangeProvider_ScrollIntoView, uiautomationcore/ITextRangeProvider::ScrollIntoView, winauto.uiauto_ITextRangeProvider_ScrollIntoView
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
 - ITextRangeProvider::ScrollIntoView
 - uiautomationcore/ITextRangeProvider::ScrollIntoView
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
 - ITextRangeProvider.ScrollIntoView
---

# ITextRangeProvider::ScrollIntoView


## -description

Causes the text control to scroll vertically until the text range is visible in the viewport.

## -parameters

### -param alignToTop [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

TRUE if the text control should be scrolled so the text range is flush with the top of the viewport; 
				FALSE if it should be flush with the bottom of the viewport.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>ITextRangeProvider::ScrollIntoView</b> respects both hidden and visible text. 

If the text range is hidden, the text control will scroll only if the hidden text has an anchor in the viewport.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>