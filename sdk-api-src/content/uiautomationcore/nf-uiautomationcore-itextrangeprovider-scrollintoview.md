---
UID: NF:uiautomationcore.ITextRangeProvider.ScrollIntoView
title: ITextRangeProvider::ScrollIntoView
author: windows-sdk-content
description: Causes the text control to scroll vertically until the text range is visible in the viewport.
old-location: winauto\uiauto_ITextRangeProvider_ScrollIntoView.htm
tech.root: WinAuto
ms.assetid: 58044de0-124f-4efd-a14f-4865f3278421
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: ITextRangeProvider interface [Windows Accessibility],ScrollIntoView method, ITextRangeProvider.ScrollIntoView, ITextRangeProvider::ScrollIntoView, ScrollIntoView, ScrollIntoView method [Windows Accessibility], ScrollIntoView method [Windows Accessibility],ITextRangeProvider interface, uiauto.uiauto_ITextRangeProvider_ScrollIntoView, uiauto_ITextRangeProvider_ScrollIntoView, uiautomationcore/ITextRangeProvider::ScrollIntoView, winauto.uiauto_ITextRangeProvider_ScrollIntoView
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITextRangeProvider.ScrollIntoView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextRangeProvider::ScrollIntoView


## -description


Causes the text control to scroll vertically until the text range is visible in the viewport. 


## -parameters




### -param alignToTop [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE if the text control should be scrolled so the text range is flush with the top of the viewport; 
				FALSE if it should be flush with the bottom of the viewport. 



## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>ITextRangeProvider::ScrollIntoView</b> respects both hidden and visible text. 

If the text range is hidden, the text control will scroll only if the hidden text has an anchor in the viewport.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

