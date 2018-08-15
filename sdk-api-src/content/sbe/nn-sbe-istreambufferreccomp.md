---
UID: NN:sbe.IStreamBufferRecComp
title: IStreamBufferRecComp
author: windows-sdk-content
description: The IStreamBufferRecComp interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.The Stream Buffer RecComp object exposes this interface.
old-location: mstv\istreambufferreccomp.htm
old-project: mstv
ms.assetid: 2998d606-d5ee-4dc3-a4da-57c597c6b594
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IStreamBufferRecComp, IStreamBufferRecComp interface [Microsoft TV Technologies], IStreamBufferRecComp interface [Microsoft TV Technologies],described, IStreamBufferRecCompInterface, mstv.istreambufferreccomp, sbe/IStreamBufferRecComp
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecComp
product: Windows
targetos: Windows
req.lib: 
req.dll: Sbe.dll
req.irql: 
req.product: ADAM
---

# IStreamBufferRecComp interface


## -description



The <b>IStreamBufferRecComp</b> interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.

The Stream Buffer <a href="https://msdn.microsoft.com/4f7fcdee-f6e2-4288-a11c-f0076858be67">RecComp</a> object exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecComp</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStreamBufferRecComp</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStreamBufferRecComp</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17911b5d-6ef5-45d2-83c3-e1b481544008">Append</a>
</td>
<td align="left" width="63%">
Appends an entire recording to the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ff4c918-64f7-4c64-b79b-7fe7d7783550">AppendEx</a>
</td>
<td align="left" width="63%">
Appends part of a recording to the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7355f5d-034c-404f-b6c7-02c04c87285d">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an append operation, if one is in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0dd311ac-28c7-4cb2-bc65-fe2301c53cf2">Close</a>
</td>
<td align="left" width="63%">
Closes the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d482bddc-3754-4d3c-8a9b-c0dc0afb00bb">GetCurrentLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97a8519f-2377-43e9-b1ba-7d407caa44a9">Initialize</a>
</td>
<td align="left" width="63%">
Sets the file name and the profile for the new recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecComp)</code>.




## -see-also




<a href="https://msdn.microsoft.com/b3e8703a-2b69-4262-9aaa-ff9ac8ca2f28">Stream Buffer Engine Interfaces</a>
 

 

