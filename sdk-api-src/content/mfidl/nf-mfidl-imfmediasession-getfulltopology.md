---
UID: NF:mfidl.IMFMediaSession.GetFullTopology
title: IMFMediaSession::GetFullTopology (mfidl.h)
description: Gets a topology from the Media Session.
helpviewer_keywords: ["6899dbe2-a684-487f-ab56-8631b3d5a033","GetFullTopology","GetFullTopology method [Media Foundation]","GetFullTopology method [Media Foundation]","IMFMediaSession interface","IMFMediaSession interface [Media Foundation]","GetFullTopology method","IMFMediaSession.GetFullTopology","IMFMediaSession::GetFullTopology","mf.imfmediasession_getfulltopology","mfidl/IMFMediaSession::GetFullTopology"]
old-location: mf\imfmediasession_getfulltopology.htm
tech.root: mf
ms.assetid: 6899dbe2-a684-487f-ab56-8631b3d5a033
ms.date: 12/05/2018
ms.keywords: 6899dbe2-a684-487f-ab56-8631b3d5a033, GetFullTopology, GetFullTopology method [Media Foundation], GetFullTopology method [Media Foundation],IMFMediaSession interface, IMFMediaSession interface [Media Foundation],GetFullTopology method, IMFMediaSession.GetFullTopology, IMFMediaSession::GetFullTopology, mf.imfmediasession_getfulltopology, mfidl/IMFMediaSession::GetFullTopology
req.header: mfidl.h
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
 - IMFMediaSession::GetFullTopology
 - mfidl/IMFMediaSession::GetFullTopology
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
 - IMFMediaSession.GetFullTopology
---

# IMFMediaSession::GetFullTopology


## -description

Gets a topology from the Media Session.

This method can get the current topology or a queued topology.

## -parameters

### -param dwGetFullTopologyFlags [in]

Bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfsession_getfulltopology_flags">MFSESSION_GETFULLTOPOLOGY_FLAGS</a> enumeration.

### -param TopoId [in]

The identifier of the topology. This parameter is ignored if the <i>dwGetFullTopologyFlags</i> parameter contains the <b>MFSESSION_GETFULLTOPOLOGY_CURRENT</b> flag. To get the identifier of a topology, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftopology-gettopologyid">IMFTopology::GetTopologyID</a>.

### -param ppFullTopology [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the topology. The caller must release the interface.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The Media Session has been shut down.
              

</td>
</tr>
</table>

## -remarks

If the <b>MFSESSION_GETFULLTOPOLOGY_CURRENT</b> flag is specified in the <i>dwGetFullTopologyFlags</i> parameter, the method returns the topology for the current presentation. Otherwise, the method searches all of the queued topologies for one that matches the identifier given in the <i>TopoId</i> parameter.
      

This method can be used to retrieve the topology for the current presentation or any pending presentations. It cannot be used to retrieve a topology that has already ended.
      

The topology returned in <i>ppFullTopo</i> is a full topology, not a partial topology.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasession">IMFMediaSession</a>



<a href="/windows/desktop/medfound/topoid">TOPOID</a>