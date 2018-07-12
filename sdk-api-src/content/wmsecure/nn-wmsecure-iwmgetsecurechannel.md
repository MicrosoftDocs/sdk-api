---
UID: NN:wmsecure.IWMGetSecureChannel
title: IWMGetSecureChannel
author: windows-sdk-content
description: The IWMGetSecureChannel interface is used by one communication party to get the other party's IWMSecureChannel interface.
old-location: wmformat\iwmgetsecurechannel.htm
old-project: wmformat
ms.assetid: 0ebb380a-5c14-4630-8ae4-825809f4737a
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: IWMGetSecureChannel, IWMGetSecureChannel interface [windows Media Format], IWMGetSecureChannel interface [windows Media Format],described, wmformat.iwmgetsecurechannel, wmsecure/IWMGetSecureChannel
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
 - IWMGetSecureChannel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMGetSecureChannel interface


## -description


<p class="CCE_Message">[<b>IWMGetSecureChannel</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]

The <b>IWMGetSecureChannel</b> interface is used by one communication party to get the
 other party's <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMGetSecureChannel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMGetSecureChannel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMGetSecureChannel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bda30638-10b5-4288-b885-b63485606a7f">GetPeerSecureChannelInterface</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://msdn.microsoft.com/ccf34dc2-a527-4ec4-b2d7-ea539ff50cf5">IWMSecureChannel</a> interface from the other communication party.

</td>
</tr>
</table> 

