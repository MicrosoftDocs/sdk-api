---
UID: NN:restrictederrorinfo.ILanguageExceptionErrorInfo2
title: ILanguageExceptionErrorInfo2 (restrictederrorinfo.h)
author: windows-sdk-content
description: Enables language projections to provide and retrieve error information as with ILanguageExceptionErrorInfo, with the additional benefit of working across language boundaries.
old-location: winrt\ilanguageexceptionerrorinfo2.htm
tech.root: WinRT
ms.assetid: A943EE85-F2A9-4D5E-AA6F-0C4AB8556A4C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILanguageExceptionErrorInfo2, ILanguageExceptionErrorInfo2 interface [Windows Runtime], ILanguageExceptionErrorInfo2 interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionErrorInfo2, winrt.ilanguageexceptionerrorinfo2
ms.topic: interface
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Restrictederrorinfo.idl
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
 - restrictederrorinfo.h
api_name:
 - ILanguageExceptionErrorInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageExceptionErrorInfo2 interface


## -description


Enables language projections to provide and retrieve error information as with <a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>, with the additional benefit of working across language boundaries.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionErrorInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>. <b>ILanguageExceptionErrorInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionErrorInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60026962-4E6C-4906-97D9-46BD2BCA3AC6">CapturePropagationContext</a>
</td>
<td align="left" width="63%">
Captures the context of an exception across a language boundary and across threads.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10A45EF1-AF8F-498D-B95B-FCE9EF8AB203">GetPreviousLanguageExceptionErrorInfo</a>
</td>
<td align="left" width="63%">
Retrieves the previous language exception error information object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1E5C74AE-C8C6-4D95-A836-DD47E50CF25D">GetPropagationContextHead</a>
</td>
<td align="left" width="63%">
Retrieves the propagation context head.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/625C0DAF-8AF6-43EB-BC81-2B3189CF8963">ILanguageExceptionErrorInfo</a>
 

 

