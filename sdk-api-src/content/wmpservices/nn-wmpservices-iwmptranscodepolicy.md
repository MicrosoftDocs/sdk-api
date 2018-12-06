---
UID: NN:wmpservices.IWMPTranscodePolicy
title: IWMPTranscodePolicy
author: windows-sdk-content
description: The IWMPTranscodePolicy interface provides a method implemented by DirectShow source filters to manage changing the format of digital media files.
old-location: wmp\iwmptranscodepolicy.htm
tech.root: WMP
ms.assetid: b7dbd25f-6865-44fa-9d46-e77de393ce13
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPTranscodePolicy, IWMPTranscodePolicy interface [Windows Media Player], IWMPTranscodePolicy interface [Windows Media Player],described, IWMPTranscodePolicyInterface, wmp.iwmptranscodepolicy, wmpservices/IWMPTranscodePolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - wmpservices.h
api_name:
 - IWMPTranscodePolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPTranscodePolicy interface


## -description



The <b>IWMPTranscodePolicy</b> interface provides a method implemented by DirectShow source filters to manage changing the format of digital media files.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPTranscodePolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPTranscodePolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPTranscodePolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6b43e247-cbb5-4ef1-8906-5ce7e1e58484">allowTranscode</a>
</td>
<td align="left" width="63%">
Retrieves a value specifying whether Windows Media Player is permitted to change the format of the digital media content to Windows Media Format.

</td>
</tr>
</table> 

To retrieve a pointer to the <b>IWMPTranscodePolicy</b> interface, Windows Media Player calls the <b>QueryInterface</b> method of the DirectShow source filter.
	


## -see-also




<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

