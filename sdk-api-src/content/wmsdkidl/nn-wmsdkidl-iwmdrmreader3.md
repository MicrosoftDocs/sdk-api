---
UID: NN:wmsdkidl.IWMDRMReader3
title: IWMDRMReader3
author: windows-driver-content
description: The IWMDRMReader3 interface enables content transcription by providing a method to get protection systems approved by a license.
old-location: wmformat\iwmdrmreader3.htm
old-project: wmformat
ms.assetid: 9474e06a-9519-456c-b304-efc875a4accc
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMDRMReader3, IWMDRMReader3 interface [windows Media Format], IWMDRMReader3 interface [windows Media Format],described, IWMDRMReader3Interface, wmformat.iwmdrmreader3, wmsdkidl/IWMDRMReader3
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMDRMReader3
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMDRMReader3 interface


## -description


<p class="CCE_Message">[<b>IWMDRMReader3</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMReader3</b> interface enables content transcription by providing a method to get protection systems approved by a license.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMReader3</b> interface inherits from <a href="https://msdn.microsoft.com/9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05">IWMDRMReader2</a>. <b>IWMDRMReader3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMReader3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac6f2ced-d60d-4472-8549-c52314375ac6">GetInclusionList</a>
</td>
<td align="left" width="63%">
Retrieves a list of identifiers specifying approved protection systems.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bf4ff0f3-1f78-43c4-be4d-c74209176e58">IWMDRMReader Interface</a>



<a href="https://msdn.microsoft.com/9fb7bbeb-d35f-41f7-b39a-2e5a102b5c05">IWMDRMReader2 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

