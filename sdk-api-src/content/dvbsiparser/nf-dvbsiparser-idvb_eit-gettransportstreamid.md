---
UID: NF:dvbsiparser.IDVB_EIT.GetTransportStreamId
title: IDVB_EIT::GetTransportStreamId
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_eit_gettransportstreamid.htm
tech.root: mstv
ms.assetid: 6333813c-e32c-4743-8a7b-98c0a63a66b9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetTransportStreamId method, IDVB_EIT.GetTransportStreamId, IDVB_EIT::GetTransportStreamId, IDVB_EITGetTransportStreamId, dvbsiparser/IDVB_EIT::GetTransportStreamId, mstv.idvb_eit_gettransportstreamid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dvbsiparser.h
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
 - dvbsiparser.h
api_name:
 - IDVB_EIT.GetTransportStreamId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDVB_EIT::GetTransportStreamId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the EIT.


## -parameters




### -param pwVal [out]

Pointer to a variable that receives the transport_stream_id field. This value identifies the transport stream from other transport streams in the multiplex.


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




<a href="https://msdn.microsoft.com/86280e1e-09c3-45a4-bdfb-53eda8e5700e">IDVB_EIT Interface</a>
 

 

