---
UID: NN:uiautomationcore.ITextProvider2
title: ITextProvider2
author: windows-sdk-content
description: Extends the ITextProvider interface to enable Microsoft UI Automation providers to expose textual content that is the target of an annotation, and information about a caret that belongs to the provider.
old-location: winauto\uiauto_itextprovider2.htm
old-project: WinAuto
ms.assetid: CDA6E93D-6E82-4EC4-8408-09554D039F49
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITextProvider2, ITextProvider2 interface [Windows Accessibility], ITextProvider2 interface [Windows Accessibility],described, uiautomationcore/ITextProvider2, winauto.uiauto_itextprovider2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ITextProvider2
product: Windows
targetos: Windows
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextProvider2 interface


## -description


Extends the  <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a> interface to enable Microsoft UI Automation providers to expose textual content that is the target of an annotation, and information about a caret that belongs to the provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider2</b> interface inherits from <a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>. <b>ITextProvider2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITextProvider2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9DD77361-25E8-40A3-BDF4-AFE06F9D36F4">GetCaretRange</a>
</td>
<td align="left" width="63%">
Provides a zero-length text range at the location of the caret that belongs to the text-based control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/908DEDED-1AF9-4DFF-AC1D-F06818B06925">RangeFromAnnotation</a>
</td>
<td align="left" width="63%">
Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element. 

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/62565f16-f0d6-42ff-bc36-897a2618c867">Document Control Type</a>



<a href="https://msdn.microsoft.com/8bd53f1e-731f-420b-a529-ca3f6c3fd97c">ITextProvider</a>



<a href="https://msdn.microsoft.com/dd14e608-1d21-4527-8b82-dba64ed04fda">ITextRangeProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

