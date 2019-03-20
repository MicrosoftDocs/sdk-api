---
UID: NN:tapi3if.IEnumSubStream
title: IEnumSubStream (tapi3if.h)
author: windows-sdk-content
description: The IEnumSubStream interface provides COM-standard enumeration methods for the ITSubStream interface. The ITSubStreamControl::EnumerateSubStreams method returns a pointer to IEnumSubStream.
old-location: tapi3\ienumsubstream.htm
tech.root: Tapi
ms.assetid: d9076a32-983e-48d4-b025-5fc770156df6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumSubStream, IEnumSubStream interface [TAPI 2.2], IEnumSubStream interface [TAPI 2.2],described, _tapi3_ienumsubstream, tapi3.ienumsubstream, tapi3if/IEnumSubStream
ms.topic: interface
req.header: tapi3if.h
req.include-header: Tapi3.h
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
 - tapi3if.h
api_name:
 - IEnumSubStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSubStream interface


## -description


The 
<b>IEnumSubStream</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a> interface. The 
<a href="https://msdn.microsoft.com/848d31e8-f878-4d33-b2b9-2d28e96bd14a">ITSubStreamControl::EnumerateSubStreams</a> method returns a pointer to 
<b>IEnumSubStream</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSubStream</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSubStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSubStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42f5ecba-4555-410c-97b1-65eb02cd5032">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa8c4017-09ac-44e9-a7fa-922d0588d92a">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72b91c81-8cfa-4879-bfcf-87fde38fcc79">Reset</a>
</td>
<td align="left" width="63%">
Resets to beginning of enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcf2fa1e-229a-4302-898c-f7a213584521">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

