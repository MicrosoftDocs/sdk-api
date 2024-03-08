---
UID: NF:segment.IMSVidStreamBufferSourceEvent3.COPPUnblocked
title: IMSVidStreamBufferSourceEvent3::COPPUnblocked (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["COPPUnblocked","COPPUnblocked method [Microsoft TV Technologies]","COPPUnblocked method [Microsoft TV Technologies]","IMSVidStreamBufferSourceEvent3 interface","IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies]","COPPUnblocked method","IMSVidStreamBufferSourceEvent3.COPPUnblocked","IMSVidStreamBufferSourceEvent3::COPPUnblocked","IMSVidStreamBufferSourceEvent3COPPUnblocked","mstv.imsvidstreambuffersourceevent3_coppunblocked","segment/IMSVidStreamBufferSourceEvent3::COPPUnblocked"]
old-location: mstv\imsvidstreambuffersourceevent3_coppunblocked.htm
tech.root: mstv
ms.assetid: e206253e-40af-4b61-8dcb-465a05cfa8f9
ms.date: 12/05/2018
ms.keywords: COPPUnblocked, COPPUnblocked method [Microsoft TV Technologies], COPPUnblocked method [Microsoft TV Technologies],IMSVidStreamBufferSourceEvent3 interface, IMSVidStreamBufferSourceEvent3 interface [Microsoft TV Technologies],COPPUnblocked method, IMSVidStreamBufferSourceEvent3.COPPUnblocked, IMSVidStreamBufferSourceEvent3::COPPUnblocked, IMSVidStreamBufferSourceEvent3COPPUnblocked, mstv.imsvidstreambuffersourceevent3_coppunblocked, segment/IMSVidStreamBufferSourceEvent3::COPPUnblocked
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMSVidStreamBufferSourceEvent3::COPPUnblocked
 - segment/IMSVidStreamBufferSourceEvent3::COPPUnblocked
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidStreamBufferSourceEvent3.COPPUnblocked
---

# IMSVidStreamBufferSourceEvent3::COPPUnblocked


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>COPPUnblocked</b> method is called when the content is unblocked after a <b>COPPBlocked</b> event.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

None.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidstreambuffersourceevent3">IMSVidStreamBufferSourceEvent3 Interface</a>



<a href="/windows/desktop/api/segment/nf-segment-imsvidstreambuffersourceevent3-coppblocked">IMSVidStreamBufferSourceEvent3::COPPBlocked</a>
