---
UID: NF:wmcontainer.IMFASFMultiplexer.GetNextPacket
title: IMFASFMultiplexer::GetNextPacket (wmcontainer.h)
description: Retrieves the next output ASF packet from the multiplexer.
helpviewer_keywords: ["39b9f8a0-fb26-4f46-98fd-b4636f8f88c7","GetNextPacket","GetNextPacket method [Media Foundation]","GetNextPacket method [Media Foundation]","IMFASFMultiplexer interface","IMFASFMultiplexer interface [Media Foundation]","GetNextPacket method","IMFASFMultiplexer.GetNextPacket","IMFASFMultiplexer::GetNextPacket","mf.imfasfmultiplexer_getnextpacket","wmcontainer/IMFASFMultiplexer::GetNextPacket"]
old-location: mf\imfasfmultiplexer_getnextpacket.htm
tech.root: mf
ms.assetid: 39b9f8a0-fb26-4f46-98fd-b4636f8f88c7
ms.date: 12/05/2018
ms.keywords: 39b9f8a0-fb26-4f46-98fd-b4636f8f88c7, GetNextPacket, GetNextPacket method [Media Foundation], GetNextPacket method [Media Foundation],IMFASFMultiplexer interface, IMFASFMultiplexer interface [Media Foundation],GetNextPacket method, IMFASFMultiplexer.GetNextPacket, IMFASFMultiplexer::GetNextPacket, mf.imfasfmultiplexer_getnextpacket, wmcontainer/IMFASFMultiplexer::GetNextPacket
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFMultiplexer::GetNextPacket
 - wmcontainer/IMFASFMultiplexer::GetNextPacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFMultiplexer.GetNextPacket
---

# IMFASFMultiplexer::GetNextPacket


## -description

Retrieves the next output ASF packet from the multiplexer.

## -parameters

### -param pdwStatusFlags [out]

Receives zero or more status flags. If more than one packet is waiting, the method sets the <b>ASF_STATUSFLAGS_INCOMPLETE</b> flag.

### -param ppIPacket [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a> interface of the first output sample of the data packet. The caller must release the interface.

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

The client needs to call this method, ideally after every call to <a href="/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample">IMFASFMultiplexer::ProcessSample</a>, to get the output ASF packets. Call this method in a loop as long as the <b>ASF_STATUSFLAGS_INCOMPLETE</b> flag is received.
      

If no packets are ready, the method returns <b>S_OK</b> but does not return a sample in <i>ppIPacket</i>.

## -see-also

<a href="/windows/desktop/medfound/generating-new-asf-data-packets">Generating New ASF Data Packets</a>



<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer">IMFASFMultiplexer</a>



<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>