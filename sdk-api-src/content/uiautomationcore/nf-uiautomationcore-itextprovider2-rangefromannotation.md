---
UID: NF:uiautomationcore.ITextProvider2.RangeFromAnnotation
title: ITextProvider2::RangeFromAnnotation
author: windows-sdk-content
description: Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element.
old-location: winauto\uiauto_itextprovider2_rangefromannotation.htm
old-project: WinAuto
ms.assetid: 908DEDED-1AF9-4DFF-AC1D-F06818B06925
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: ITextProvider2 interface [Windows Accessibility],RangeFromAnnotation method, ITextProvider2.RangeFromAnnotation, ITextProvider2::RangeFromAnnotation, RangeFromAnnotation, RangeFromAnnotation method [Windows Accessibility], RangeFromAnnotation method [Windows Accessibility],ITextProvider2 interface, uiautomationcore/ITextProvider2::RangeFromAnnotation, winauto.uiauto_itextprovider2_rangefromannotation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	UIAutomationCore.h
api_name:
-	ITextProvider2.RangeFromAnnotation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextProvider2::RangeFromAnnotation


## -description


Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element. 


## -parameters




### -param annotationElement [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The provider for an element that implements the <a href="https://msdn.microsoft.com/EDD711F1-9D1B-4B6B-8052-E9258759F46E">IAnnotationProvider</a> interface. The annotation element is a sibling of the element that implements the <a href="https://msdn.microsoft.com/CDA6E93D-6E82-4EC4-8408-09554D039F49">ITextProvider2</a> interface for the document.


### -param pRetVal [out, retval]

Type: <b><a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>**</b>

Receives a text range that contains the annotation target text.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/62565f16-f0d6-42ff-bc36-897a2618c867">Document Control Type</a>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/CDA6E93D-6E82-4EC4-8408-09554D039F49">ITextProvider2</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

