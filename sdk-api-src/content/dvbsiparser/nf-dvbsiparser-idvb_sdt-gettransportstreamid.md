---
UID: NF:dvbsiparser.IDVB_SDT.GetTransportStreamId
title: IDVB_SDT::GetTransportStreamId
author: windows-driver-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\idvb_sdt_gettransportstreamid.htm
old-project: mstv
ms.assetid: a4ecaf56-bc2b-46f3-94e7-aae63ad9be06
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IDVB_SDT interface, IDVB_SDT interface [Microsoft TV Technologies],GetTransportStreamId method, IDVB_SDT.GetTransportStreamId, IDVB_SDT::GetTransportStreamId, IDVB_SDTGetTransportStreamId, dvbsiparser/IDVB_SDT::GetTransportStreamId, mstv.idvb_sdt_gettransportstreamid
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IDVB_SDT.GetTransportStreamId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDVB_SDT::GetTransportStreamId


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the SDT.


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




<a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT Interface</a>
 

 

