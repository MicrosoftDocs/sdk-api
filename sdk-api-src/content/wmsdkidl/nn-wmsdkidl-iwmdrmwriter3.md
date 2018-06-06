---
UID: NN:wmsdkidl.IWMDRMWriter3
title: IWMDRMWriter3
author: windows-sdk-content
description: The IWMDRMWriter3 interface enables writing of encrypted stream samples for importing protected content.An IWMDRMWriter3 interface exists for every writer object when linking to WMStubDRM.lib.
old-location: wmformat\iwmdrmwriter3.htm
old-project: wmformat
ms.assetid: b300b97b-e558-4c33-a84a-e92c28a3a606
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWMDRMWriter3, IWMDRMWriter3 interface [windows Media Format], IWMDRMWriter3 interface [windows Media Format],described, IWMDRMWriter3Interface, wmformat.iwmdrmwriter3, wmsdkidl/IWMDRMWriter3
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
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
 - IWMDRMWriter3
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMWriter3 interface


## -description


<p class="CCE_Message">[<b>IWMDRMWriter3</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMWriter3</b> interface enables writing of encrypted stream samples for importing protected content.

An <b>IWMDRMWriter3</b> interface exists for every writer object when linking to WMStubDRM.lib. You can obtain a pointer to an instance of this interface by calling the <b>QueryInterface</b> method of any interface of a writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMWriter3</b> interface inherits from <a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter</a> and <a href="https://msdn.microsoft.com/8511b464-1f47-4184-9cb7-9aca0cb6660f">IWMDRMWriter2</a>. <b>IWMDRMWriter3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMWriter3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42208d02-8384-494d-b7ae-53072b795723">SetProtectStreamSamples</a>
</td>
<td align="left" width="63%">
Configures the writer to accept encrypted stream samples.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fd466cf8-b1f8-49aa-a486-8fd347b29178">IWMDRMWriter</a>



<a href="https://msdn.microsoft.com/8511b464-1f47-4184-9cb7-9aca0cb6660f">IWMDRMWriter2</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

