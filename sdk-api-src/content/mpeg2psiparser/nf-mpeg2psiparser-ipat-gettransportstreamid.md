---
UID: NF:mpeg2psiparser.IPAT.GetTransportStreamId
title: IPAT::GetTransportStreamId
author: windows-sdk-content
description: The GetTransportStreamId method returns the transport stream identifier (TSID) for the PAT.
old-location: mstv\ipat_gettransportstreamid.htm
old-project: mstv
ms.assetid: 3a13bb01-47d6-4737-9e66-169def727b5e
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTransportStreamId, GetTransportStreamId method [Microsoft TV Technologies], GetTransportStreamId method [Microsoft TV Technologies],IPAT interface, IPAT interface [Microsoft TV Technologies],GetTransportStreamId method, IPAT.GetTransportStreamId, IPAT::GetTransportStreamId, IPATGetTransportStreamId, mpeg2psiparser/IPAT::GetTransportStreamId, mstv.ipat_gettransportstreamid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mpeg2psiparser.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPAT.GetTransportStreamId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPAT::GetTransportStreamId


## -description



The <b>GetTransportStreamId</b> method returns the transport stream identifier (TSID) for the PAT.




## -parameters




### -param pwVal [out]

Receives the transport_stream_id field.


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




<a href="https://msdn.microsoft.com/31b0e558-0f22-4761-a964-1908c2835478">IPAT Interface</a>
 

 

