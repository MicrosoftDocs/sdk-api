---
UID: NF:atscpsipparser.IATSC_VCT.GetTransportStreamId
title: IATSC_VCT::GetTransportStreamId (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct_gettransportstreamid.htm
tech.root: mstv
ms.assetid: 0c3261e8-c671-48c7-b07c-59ce74b13c76
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetTransportStreamId method, IATSC_VCT.GetTransportStreamId, IATSC_VCT::GetTransportStreamId, IATSC_VCTGetTransportStreamId, atscpsipparser/IATSC_VCT::GetTransportStreamId, mstv.iatsc_vct_gettransportstreamid
ms.topic: method
req.header: atscpsipparser.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_VCT.GetTransportStreamId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_VCT::GetTransportStreamId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the entire VCT.


## -parameters




### -param pwVal [out]

Receives the transport_stream_id field. This value should match the value that appears in the program association table (PAT).


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3ff9cd6e-0d25-462c-93a7-2399395f68b0">IATSC_VCT Interface</a>
 

 

