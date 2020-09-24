---
UID: NF:mfidl.IMFTopoLoader.Load
title: IMFTopoLoader::Load (mfidl.h)
description: Creates a fully loaded topology from the input partial topology.
helpviewer_keywords: ["02ce47db-54a1-456a-a763-c62039aea2c9","IMFTopoLoader interface [Media Foundation]","Load method","IMFTopoLoader.Load","IMFTopoLoader::Load","Load","Load method [Media Foundation]","Load method [Media Foundation]","IMFTopoLoader interface","mf.imftopoloader_load","mfidl/IMFTopoLoader::Load"]
old-location: mf\imftopoloader_load.htm
tech.root: mf
ms.assetid: 02ce47db-54a1-456a-a763-c62039aea2c9
ms.date: 12/05/2018
ms.keywords: 02ce47db-54a1-456a-a763-c62039aea2c9, IMFTopoLoader interface [Media Foundation],Load method, IMFTopoLoader.Load, IMFTopoLoader::Load, Load, Load method [Media Foundation], Load method [Media Foundation],IMFTopoLoader interface, mf.imftopoloader_load, mfidl/IMFTopoLoader::Load
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
 - IMFTopoLoader::Load
 - mfidl/IMFTopoLoader::Load
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
 - IMFTopoLoader.Load
---

# IMFTopoLoader::Load


## -description

Creates a fully loaded topology from the input partial topology.

## -parameters

### -param pInputTopo [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the partial topology to be resolved.

### -param ppOutputTopo [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the completed topology. The caller must release the interface.

### -param pCurrentTopo [in]

A pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the previous full topology. The topology loader can re-use objects from this topology in the new topology. This parameter can be <b>NULL</b>. See Remarks.

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
<dt><b>MF_E_TOPO_SINK_ACTIVATES_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
One or more output nodes contain <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointers. The caller must bind the output nodes to media sinks. See  <a href="/windows/desktop/medfound/binding-output-nodes-to-media-sinks">Binding Output Nodes to Media Sinks</a>.

</td>
</tr>
</table>

## -remarks

This method creates any intermediate transforms that are needed to complete the topology. It also sets the input and output media types on all of the objects in the topology. If the method succeeds, the full topology is returned in the <i>ppOutputTopo</i> parameter.
      

You can use the <i>pCurrentTopo</i> parameter to provide a full topology that was previously loaded. If this topology contains objects that are needed in the new topology, the topology loader can re-use them without creating them again. This caching can potentially make the process faster. The objects from <i>pCurrentTopo</i> will not be reconfigured, so you can specify a topology that is actively streaming data. For example, while a topology is still running, you can pre-load the next topology.
      

Before calling this method, you must ensure that the output nodes in the partial topology have valid <a href="/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink">IMFStreamSink</a> pointers, not <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointers. The Media Session automatically performs this action inside the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> method. However, if you call <b>Load</b> before calling <b>SetTopology</b>, you must bind the output nodes manually. For more information, see <a href="/windows/desktop/medfound/binding-output-nodes-to-media-sinks">Binding Output Nodes to Media Sinks</a>.

## -see-also

<a href="/windows/desktop/medfound/advanced-topology-building">Advanced Topology Building</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imftopoloader">IMFTopoLoader</a>



<a href="/windows/desktop/medfound/topologies">Topologies</a>