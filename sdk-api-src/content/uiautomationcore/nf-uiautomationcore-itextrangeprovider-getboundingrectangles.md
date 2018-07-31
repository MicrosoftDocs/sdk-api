---
UID: NF:uiautomationcore.ITextRangeProvider.GetBoundingRectangles
title: ITextRangeProvider::GetBoundingRectangles
author: windows-sdk-content
description: Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.
old-location: winauto\uiauto_ITextRangeProvider_GetBoundingRectangles.htm
old-project: WinAuto
ms.assetid: 2ca1d170-538b-4dc2-83f3-850e1873c0d1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetBoundingRectangles, GetBoundingRectangles method [Windows Accessibility], GetBoundingRectangles method [Windows Accessibility],ITextRangeProvider interface, ITextRangeProvider interface [Windows Accessibility],GetBoundingRectangles method, ITextRangeProvider.GetBoundingRectangles, ITextRangeProvider::GetBoundingRectangles, uiauto.uiauto_ITextRangeProvider_GetBoundingRectangles, uiauto_ITextRangeProvider_GetBoundingRectangles, uiautomationcore/ITextRangeProvider::GetBoundingRectangles, winauto.uiauto_ITextRangeProvider_GetBoundingRectangles
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - ITextRangeProvider.GetBoundingRectangles
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextRangeProvider::GetBoundingRectangles


## -description


Retrieves a collection of bounding rectangles for each fully or partially visible line of text in a text range.
        


## -parameters




### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9ec8025b-4763-4526-ab45-390c5d8b3b1e">SAFEARRAY</a>**</b>

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



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/07e87cfd-d565-41b5-a68d-b99dd191fa95">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

