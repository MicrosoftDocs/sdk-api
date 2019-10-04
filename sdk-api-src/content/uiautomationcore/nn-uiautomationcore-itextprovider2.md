---
UID: NN:uiautomationcore.ITextProvider2
title: ITextProvider2 (uiautomationcore.h)
author: windows-sdk-content
description: Extends the ITextProvider interface to enable Microsoft UI Automation providers to expose textual content that is the target of an annotation, and information about a caret that belongs to the provider.
old-location: winauto\uiauto_itextprovider2.htm
tech.root: WinAuto
ms.assetid: CDA6E93D-6E82-4EC4-8408-09554D039F49
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITextProvider2, ITextProvider2 interface [Windows Accessibility], ITextProvider2 interface [Windows Accessibility],described, uiautomationcore/ITextProvider2, winauto.uiauto_itextprovider2
ms.topic: interface
f1_keywords: 
 - "uiautomationcore/ITextProvider2"
dev_langs:
 - c++
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
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ITextProvider2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITextProvider2 interface


## -description


Extends the  <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a> interface to enable Microsoft UI Automation providers to expose textual content that is the target of an annotation, and information about a caret that belongs to the provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITextProvider2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>. <b>ITextProvider2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-getcaretrange">GetCaretRange</a>
</td>
<td align="left" width="63%">
Provides a zero-length text range at the location of the caret that belongs to the text-based control.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itextprovider2-rangefromannotation">RangeFromAnnotation</a>
</td>
<td align="left" width="63%">
Exposes a text range that contains the text that is the target of the annotation associated with the specified annotation element. 

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-supportdocumentcontroltype">Document Control Type</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextprovider">ITextProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itextrangeprovider">ITextRangeProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-ui-automation-textpattern-overview">UI Automation Support for Textual Content</a>
 

 

