---
UID: NF:segment.IMSVidGenericSink2.ResetFilterList
title: IMSVidGenericSink2::ResetFilterList (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. .helpviewer_keywords: ["IMSVidGenericSink2 interface [Microsoft TV Technologies]","ResetFilterList method","IMSVidGenericSink2.ResetFilterList","IMSVidGenericSink2::ResetFilterList","IMSVidGenericSink2ResetFilterList","ResetFilterList","ResetFilterList method [Microsoft TV Technologies]","ResetFilterList method [Microsoft TV Technologies]","IMSVidGenericSink2 interface","mstv.imsvidgenericsink2_resetfilterlist","segment/IMSVidGenericSink2::ResetFilterList"]
old-location: mstv\imsvidgenericsink2_resetfilterlist.htm
tech.root: mstv
ms.assetid: fc899c48-703a-4bdc-849e-73633ae748d0
ms.date: 12/05/2018
ms.keywords: IMSVidGenericSink2 interface [Microsoft TV Technologies],ResetFilterList method, IMSVidGenericSink2.ResetFilterList, IMSVidGenericSink2::ResetFilterList, IMSVidGenericSink2ResetFilterList, ResetFilterList, ResetFilterList method [Microsoft TV Technologies], ResetFilterList method [Microsoft TV Technologies],IMSVidGenericSink2 interface, mstv.imsvidgenericsink2_resetfilterlist, segment/IMSVidGenericSink2::ResetFilterList
f1_keywords:
- segment/IMSVidGenericSink2.ResetFilterList
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- segment.h
api_name:
- IMSVidGenericSink2.ResetFilterList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidGenericSink2::ResetFilterList


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>




The <b>ResetFilterList</b> method clears the list of filters that were added using <a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidgenericsink2-addfilter">IMSVidGenericSink2::AddFilter</a>.


## -parameters






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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/segment/nn-segment-imsvidgenericsink2">IMSVidGenericSink2 Interface</a>
 

 

