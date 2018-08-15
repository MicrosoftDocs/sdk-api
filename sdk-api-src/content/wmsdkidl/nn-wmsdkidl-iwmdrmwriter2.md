---
UID: NN:wmsdkidl.IWMDRMWriter2
title: IWMDRMWriter2
author: windows-sdk-content
description: The IWMDRMWriter2 interface provides a method that enables you to write content encrypted with Windows Media DRM 10 for Network Devices.An IWMDRMWriter2 interface exists for every writer object.
old-location: wmformat\iwmdrmwriter2.htm
old-project: wmformat
ms.assetid: 8511b464-1f47-4184-9cb7-9aca0cb6660f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMDRMWriter2, IWMDRMWriter2 interface [windows Media Format], IWMDRMWriter2 interface [windows Media Format],described, IWMDRMWriter2Interface, wmformat.iwmdrmwriter2, wmsdkidl/IWMDRMWriter2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMDRMWriter2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMWriter2 interface


## -description


<p class="CCE_Message">[<b>IWMDRMWriter2</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter2</b> interface provides a method that enables you to write content encrypted with Windows Media DRM 10 for Network Devices.

An <b>IWMDRMWriter2</b> interface exists for every writer object. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface of a writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMWriter2</b> interface inherits from <a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter</a>. <b>IWMDRMWriter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMWriter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecbc7dda-de24-40ce-9c42-44a14ab63881">SetWMDRMNetEncryption</a>
</td>
<td align="left" width="63%">
Configures the writer to receive input samples encoded for Windows Media DRM 10 for Network Devices delivery.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>
 

 

