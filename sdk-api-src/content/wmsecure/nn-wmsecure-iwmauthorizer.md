---
UID: NN:wmsecure.IWMAuthorizer
title: IWMAuthorizer
author: windows-sdk-content
description: Provides access to certificates.
old-location: wmformat\iwmauthorizer.htm
old-project: wmformat
ms.assetid: eece7e36-7c3e-4bc4-9b5a-8142a062dbce
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: IWMAuthorizer, IWMAuthorizer interface [windows Media Format], IWMAuthorizer interface [windows Media Format],described, wmformat.iwmauthorizer, wmsecure/IWMAuthorizer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsecure.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WMT_WATERMARK_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsecure.h
api_name:
 - IWMAuthorizer
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMAuthorizer interface


## -description


<p class="CCE_Message">[<b>IWMAuthorizer</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

Provides access to certificates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMAuthorizer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMAuthorizer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMAuthorizer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e165356c-b14b-47dc-b046-a74499251cab">GetCert</a>
</td>
<td align="left" width="63%">
Retrieves the specified certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afe8a924-3d2b-42e6-9700-a6075f51ff10">GetCertCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of certificates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/575df33a-b29e-43eb-84c2-6f9875f26196">GetSharedData</a>
</td>
<td align="left" width="63%">
Retrieves shared  data for the specified certificate.

</td>
</tr>
</table> 

