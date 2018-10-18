---
UID: NN:dshowasf.IConfigAsfWriter2
title: IConfigAsfWriter2
author: windows-sdk-content
description: The IConfigAsfWriter2 interface inherits from the IConfigAsfWriter interface and provides additional methods to support the capabilities introduced in the Windows Media Format 9 Series SDK such as two-pass encoding and support for interlaced output.
old-location: wmformat\iconfigasfwriter2.htm
tech.root: wmformat
ms.assetid: c597ac93-7ec4-43dd-bc8a-16ba9c4611f4
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IConfigAsfWriter2, IConfigAsfWriter2 interface [windows Media Format], IConfigAsfWriter2 interface [windows Media Format],described, IConfigAsfWriter2Interface, dshowasf/IConfigAsfWriter2, wmformat.iconfigasfwriter2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Requires Dshowasf.h, Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - dshowasf.h
api_name:
 - IConfigAsfWriter2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter2 interface


## -description



The <b>IConfigAsfWriter2</b> interface inherits from the <a href="https://msdn.microsoft.com/481c0819-c18d-42e3-aebe-f156c414428d">IConfigAsfWriter</a> interface and provides additional methods to support the capabilities introduced in the Windows Media Format 9 Series SDK such as two-pass encoding and support for interlaced output.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigAsfWriter2</b> interface inherits from <a href="https://msdn.microsoft.com/481c0819-c18d-42e3-aebe-f156c414428d">IConfigAsfWriter</a>. <b>IConfigAsfWriter2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IConfigAsfWriter2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81d915a1-6190-46e3-a5cb-7f5fc242b8dd">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6687af7-f3cd-4e92-9c76-dddff9063fa0">ResetMultiPassState</a>
</td>
<td align="left" width="63%">
Resets the filter when a preprocessing encoding pass is canceled before it is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8067fb2-c379-4b26-b4f7-c790604e3edc">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f645a742-e6dc-4041-8a56-3bbb5188a9a9">StreamNumFromPin</a>
</td>
<td align="left" width="63%">
Retrieves the stream number associated with the specified input pin.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/481c0819-c18d-42e3-aebe-f156c414428d">IConfigAsfWriter</a>
 

 

