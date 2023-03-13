---
UID: NF:uiautomationcore.ITextRangeProvider.GetBoundingRectangles
title: ITextRangeProvider::GetBoundingRectangles (uiautomationcore.h)
description: Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range. (ITextRangeProvider.GetBoundingRectangles)
helpviewer_keywords: ["GetBoundingRectangles","GetBoundingRectangles method [Windows Accessibility]","GetBoundingRectangles method [Windows Accessibility]","ITextRangeProvider interface","ITextRangeProvider interface [Windows Accessibility]","GetBoundingRectangles method","ITextRangeProvider.GetBoundingRectangles","ITextRangeProvider::GetBoundingRectangles","uiauto.uiauto_ITextRangeProvider_GetBoundingRectangles","uiauto_ITextRangeProvider_GetBoundingRectangles","uiautomationcore/ITextRangeProvider::GetBoundingRectangles","winauto.uiauto_ITextRangeProvider_GetBoundingRectangles"]
old-location: winauto\uiauto_ITextRangeProvider_GetBoundingRectangles.htm
tech.root: WinAuto
ms.assetid: 2ca1d170-538b-4dc2-83f3-850e1873c0d1
ms.date: 12/05/2018
ms.keywords: GetBoundingRectangles, GetBoundingRectangles method [Windows Accessibility], GetBoundingRectangles method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetBoundingRectangles method, ITextRangeProvider.GetBoundingRectangles, ITextRangeProvider::GetBoundingRectangles, uiauto.uiauto_ITextRangeProvider_GetBoundingRectangles, uiauto_ITextRangeProvider_GetBoundingRectangles, uiautomationcore/ITextRangeProvider::GetBoundingRectangles, winauto.uiauto_ITextRangeProvider_GetBoundingRectangles
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
 - ITextRangeProvider::GetBoundingRectangles
 - uiautomationcore/ITextRangeProvider::GetBoundingRectangles
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
 - ITextRangeProvider.GetBoundingRectangles
---

# ITextRangeProvider::GetBoundingRectangles


## -description

Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.

## -parameters

### -param pRetVal [out, retval]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>**</b>

Receives a pointer to one of the following.
                

<ul>
<li>An array of bounding rectangles 
                for each full or partial line of text in a text range.
                </li>
<li>An empty array for a degenerate range.
                </li>
<li>An empty array for a text range that has screen coordinates placing it completely 
                off-screen, scrolled out of view, or obscured by an overlapping window.
                </li>
</ul>
This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
