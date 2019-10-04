---
UID: NN:sbe.IEnumStreamBufferRecordingAttrib
title: IEnumStreamBufferRecordingAttrib (sbe.h)
author: windows-sdk-content
description: The IEnumStreamBufferRecordingAttrib interface enumerates a collection of attributes on a stream buffer file.
old-location: mstv\ienumstreambufferrecordingattrib.htm
tech.root: mstv
ms.assetid: 668d2e04-74fa-41d7-b238-ec737a4441ca
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumStreamBufferRecordingAttrib, IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies], IEnumStreamBufferRecordingAttrib interface [Microsoft TV Technologies],described, IEnumStreamBufferRecordingAttribInterface, mstv.ienumstreambufferrecordingattrib, sbe/IEnumStreamBufferRecordingAttrib
ms.topic: interface
f1_keywords: 
 - "sbe/IEnumStreamBufferRecordingAttrib"
dev_langs:
 - c++
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
 - IEnumStreamBufferRecordingAttrib
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumStreamBufferRecordingAttrib interface


## -description



The <b>IEnumStreamBufferRecordingAttrib</b> interface enumerates a collection of attributes on a stream buffer file. <i>Attributes</i> are metadata that describe the physical file (such as the bit rate and the duration) or the content of the file (such as the author or title). To obtain this interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambufferrecordingattribute-enumattributes">IStreamBufferRecordingAttribute::EnumAttributes</a> method.

This interface implements a standard Component Object Model (COM) collection object. For more information on COM collections, see the <b>IEnumXXXX</b> topic in the Microsoft Platform SDK. The collection object represents a snapshot of the attributes when the collection is created; the collection is not updated automatically.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumStreamBufferRecordingAttrib</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumStreamBufferRecordingAttrib</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumStreamBufferRecordingAttrib</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-ienumstreambufferrecordingattrib-clone">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-ienumstreambufferrecordingattrib-next">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of attributes in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-ienumstreambufferrecordingattrib-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-ienumstreambufferrecordingattrib-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over a specified number of attributes.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IEnumStreamBufferRecordingAttrib)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-engine-interfaces">Stream Buffer Engine Interfaces</a>
 

 

