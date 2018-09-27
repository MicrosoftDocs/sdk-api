---
UID: NN:dshowasf.IConfigAsfWriter2
title: IConfigAsfWriter2
author: windows-sdk-content
description: The IConfigAsfWriter2 interface extends the IConfigAsfWriter interface, which configures the WM ASF Writer filter.
old-location: dshow\iconfigasfwriter2.htm
tech.root: DirectShow
ms.assetid: fd931a95-3678-46de-8f17-9e7c27087398
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: IConfigAsfWriter2, IConfigAsfWriter2 interface [DirectShow], IConfigAsfWriter2 interface [DirectShow],described, IConfigAsfWriter2Interface, dshow.iconfigasfwriter2, dshowasf/IConfigAsfWriter2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dshowasf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dshowasf.h
api_name:
 - IConfigAsfWriter2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConfigAsfWriter2 interface


## -description



The <code>IConfigAsfWriter2</code> interface extends the <a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter</a> interface, which configures the <a href="https://msdn.microsoft.com/1b12f65f-8d77-4d38-aad9-92bb15cc0426">WM ASF Writer</a> filter. The <code>IConfigAsfWriter2</code> interface provides additional methods to support the capabilities introduced in the Windows Media Format 9 Series SDK, such as two-pass encoding and support for interlaced output.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IConfigAsfWriter2</b> interface inherits from <a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter</a>. <b>IConfigAsfWriter2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/2a875d02-3814-46a1-9eee-61bad36475fc">GetParam</a>
</td>
<td align="left" width="63%">
Retrieves the current value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ca2ec239-ffb9-4030-9160-77a0c9be0a07">ResetMultiPassState</a>
</td>
<td align="left" width="63%">
Resets the filter when a preprocessing encoding pass is canceled before it is completed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0294837c-0cf2-4a05-bef4-16d13864f759">SetParam</a>
</td>
<td align="left" width="63%">
Sets the value of the specified filter configuration parameter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/374331ec-6665-4ed9-b4ee-6d33b1e2ef2c">StreamNumFromPin</a>
</td>
<td align="left" width="63%">
Retrieves the stream number associated with the specified input pin.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/dffda43a-5831-4889-864f-81351b9e2bb3">Creating ASF Files in DirectShow</a>



<a href="https://msdn.microsoft.com/50fd7825-4844-4a7f-b949-4abfff5ef30f">IConfigAsfWriter</a>
 

 

