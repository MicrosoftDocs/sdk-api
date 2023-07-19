---
UID: NF:segment.IMSVidXDS.get_ChannelChangeInterface
title: IMSVidXDS::get_ChannelChangeInterface (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. .
helpviewer_keywords: ["IMSVidXDS interface [Microsoft TV Technologies]","get_ChannelChangeInterface method","IMSVidXDS.get_ChannelChangeInterface","IMSVidXDS::get_ChannelChangeInterface","IMSVidXDSgetChannelChangeInterface","get_ChannelChangeInterface","get_ChannelChangeInterface method [Microsoft TV Technologies]","get_ChannelChangeInterface method [Microsoft TV Technologies]","IMSVidXDS interface","mstv.imsvidxds_get_channelchangeinterface","segment/IMSVidXDS::get_ChannelChangeInterface"]
old-location: mstv\imsvidxds_get_channelchangeinterface.htm
tech.root: mstv
ms.assetid: 078bd274-b8dc-425b-b14f-3dacff6744bb
ms.date: 12/05/2018
ms.keywords: IMSVidXDS interface [Microsoft TV Technologies],get_ChannelChangeInterface method, IMSVidXDS.get_ChannelChangeInterface, IMSVidXDS::get_ChannelChangeInterface, IMSVidXDSgetChannelChangeInterface, get_ChannelChangeInterface, get_ChannelChangeInterface method [Microsoft TV Technologies], get_ChannelChangeInterface method [Microsoft TV Technologies],IMSVidXDS interface, mstv.imsvidxds_get_channelchangeinterface, segment/IMSVidXDS::get_ChannelChangeInterface
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
 - IMSVidXDS::get_ChannelChangeInterface
 - segment/IMSVidXDS::get_ChannelChangeInterface
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
 - IMSVidXDS.get_ChannelChangeInterface
---

# IMSVidXDS::get_ChannelChangeInterface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>




The <b>get_ChannelChangeInterface</b> method retrieves a pointer to an interface that raises an event when the channel is changed.

## -parameters

### -param punkCC [out]

Receives a pointer to the <b>IUnknown</b> interface. The caller must release the interface.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/msvidxds">IMSVidXDS Interface</a>