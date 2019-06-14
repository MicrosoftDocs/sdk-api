---
UID: NN:restrictederrorinfo.ILanguageExceptionErrorInfo
title: ILanguageExceptionErrorInfo (restrictederrorinfo.h)
author: windows-sdk-content
description: Enables retrieving the IUnknown pointer stored in the error info with the call to RoOriginateLanguageException.
old-location: winrt\ilanguageexceptionerrorinfo.htm
tech.root: WinRT
ms.assetid: 625C0DAF-8AF6-43EB-BC81-2B3189CF8963
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ILanguageExceptionErrorInfo, ILanguageExceptionErrorInfo interface [Windows Runtime], ILanguageExceptionErrorInfo interface [Windows Runtime],described, restrictederrorinfo/ILanguageExceptionErrorInfo, winrt.ilanguageexceptionerrorinfo
ms.topic: interface
req.header: restrictederrorinfo.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - ILanguageExceptionErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILanguageExceptionErrorInfo interface


## -description


Enables retrieving the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer stored in the error info with the call to RoOriginateLanguageException.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageExceptionErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILanguageExceptionErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageExceptionErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/restrictederrorinfo/nf-restrictederrorinfo-ilanguageexceptionerrorinfo-getlanguageexception">GetLanguageException</a>
</td>
<td align="left" width="63%">
Gets the stored <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> object from the error object.

</td>
</tr>
</table> 

