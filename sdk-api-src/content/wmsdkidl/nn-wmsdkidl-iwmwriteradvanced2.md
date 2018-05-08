---
UID: NN:wmsdkidl.IWMWriterAdvanced2
title: IWMWriterAdvanced2
author: windows-driver-content
description: The IWMWriterAdvanced2 interface provides the ability to set and retrieve named settings for an input.IWMWriterAdvanced2 exists for every instance of the writer object. To obtain a pointer to this interface, call QueryInterface on the writer object.
old-location: wmformat\iwmwriteradvanced2.htm
old-project: wmformat
ms.assetid: 94790b67-690c-4a0f-9b82-801bfcec9eb0
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMWriterAdvanced2, IWMWriterAdvanced2 interface [windows Media Format], IWMWriterAdvanced2 interface [windows Media Format],described, IWMWriterAdvanced2Interface, wmformat.iwmwriteradvanced2, wmsdkidl/IWMWriterAdvanced2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMWriterAdvanced2
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterAdvanced2 interface


## -description



The <b>IWMWriterAdvanced2</b> interface provides the ability to set and retrieve named settings for an input.

<b>IWMWriterAdvanced2</b> exists for every instance of the writer object. To obtain a pointer to this interface, call <b>QueryInterface</b> on the writer object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMWriterAdvanced2</b> interface inherits from <a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced</a>. <b>IWMWriterAdvanced2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMWriterAdvanced2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aea0bc6-94e7-41ab-aec3-7366f183bb01">GetInputSetting</a>
</td>
<td align="left" width="63%">
Retrieves a setting for a particular input by name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a920bfe8-1f95-4957-b6c4-9749d5e10ee3">SetInputSetting</a>
</td>
<td align="left" width="63%">
Specifies a named setting for a particular input.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see <a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>.



## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/082cd277-157d-42a4-bf37-e47d16f90c7a">IWMWriterAdvanced Interface</a>



<a href="https://msdn.microsoft.com/99f7e4f7-0080-498d-b4f1-960c4955b4db">IWMWriterAdvanced3 Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8058b7fe-7d02-4572-ad43-6867d4ceb7e9">Writer Object</a>



<a href="https://msdn.microsoft.com/d722b676-bf65-4f91-8118-bb12d3bbb6cb">Writing ASF Files</a>
 

 

