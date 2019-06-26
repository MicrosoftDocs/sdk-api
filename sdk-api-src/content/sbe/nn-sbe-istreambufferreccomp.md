---
UID: NN:sbe.IStreamBufferRecComp
title: IStreamBufferRecComp (sbe.h)
author: windows-sdk-content
description: The IStreamBufferRecComp interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.The Stream Buffer RecComp object exposes this interface.
old-location: mstv\istreambufferreccomp.htm
tech.root: mstv
ms.assetid: 2998d606-d5ee-4dc3-a4da-57c597c6b594
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamBufferRecComp, IStreamBufferRecComp interface [Microsoft TV Technologies], IStreamBufferRecComp interface [Microsoft TV Technologies],described, IStreamBufferRecCompInterface, mstv.istreambufferreccomp, sbe/IStreamBufferRecComp
ms.topic: interface
f1_keywords: 
 - "sbe/IStreamBufferRecComp"
req.header: sbe.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferRecComp interface


## -description



The <b>IStreamBufferRecComp</b> interface is used to create new content recordings by concatenating existing recordings. The new recording can be created from a mix of reference and content recordings.

The Stream Buffer <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/reccomp-object">RecComp</a> object exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStreamBufferRecComp</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStreamBufferRecComp</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-append">Append</a>
</td>
<td align="left" width="63%">
Appends an entire recording to the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-appendex">AppendEx</a>
</td>
<td align="left" width="63%">
Appends part of a recording to the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-cancel">Cancel</a>
</td>
<td align="left" width="63%">
Cancels an append operation, if one is in progress.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-close">Close</a>
</td>
<td align="left" width="63%">
Closes the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-getcurrentlength">GetCurrentLength</a>
</td>
<td align="left" width="63%">
Retrieves the length of the target file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferreccomp-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Sets the file name and the profile for the new recording.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IStreamBufferRecComp)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

