---
UID: NF:uiautomationcore.ITextProvider.GetVisibleRanges
title: ITextProvider::GetVisibleRanges (uiautomationcore.h)
author: windows-sdk-content
description: Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.
old-location: winauto\uiauto_ITextProvider_GetVisibleRanges.htm
tech.root: WinAuto
ms.assetid: dc706d1d-b32d-4bc3-b65a-c42b38f06a93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVisibleRanges, GetVisibleRanges method [Windows Accessibility], GetVisibleRanges method [Windows Accessibility],ITextProvider interface, ITextProvider interface [Windows Accessibility],GetVisibleRanges method, ITextProvider.GetVisibleRanges, ITextProvider::GetVisibleRanges, uiauto.uiauto_ITextProvider_GetVisibleRanges, uiauto_ITextProvider_GetVisibleRanges, uiautomationcore/ITextProvider::GetVisibleRanges, winauto.uiauto_ITextProvider_GetVisibleRanges
ms.topic: method
f1_keywords: ["uiautomationcore/ITextProvider.GetVisibleRanges"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextProvider.GetVisibleRanges
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextProvider::GetVisibleRanges


## -description


Retrieves an array of disjoint text ranges from a text-based control where each text range represents a contiguous span of visible text.  


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the address of an array of pointers to the 
                <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a> interfaces of the visible 
                text ranges or an empty array. 
                A <b>NULL</b> reference is never returned.
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the visible text consists of one contiguous span of text, the <i>pRetVal</i> array should contain a single text range that represents all of the visible text. 

If the visible text consists of multiple, disjoint spans of text, the <i>pRetVal</i> array should contain one text range for each visible span, beginning with the first visible span, and ending with the last visible span. Disjoint spans of visible text can occur when the content of a text-based control is partially obscured 
            by an overlapping window or other object, or when a text-based  control with multiple pages or columns 
            has content that is partially scrolled out of view.
            

<b>ITextProvider::GetVisibleRanges</b> should return  a degenerate (empty) text range if no text is visible, if all text is scrolled out of view, or if the text-based control contains no text.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
 

 

