---
UID: NF:mfidl.IMFTopoLoader.Load
title: IMFTopoLoader::Load method
author: windows-driver-content
description: Creates a fully loaded topology from the input partial topology.
old-location: mf\imftopoloader_load.htm
old-project: medfound
ms.assetid: 02ce47db-54a1-456a-a763-c62039aea2c9
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 02ce47db-54a1-456a-a763-c62039aea2c9, IMFTopoLoader, IMFTopoLoader interface [Media Foundation], Load method, IMFTopoLoader::Load, Load method [Media Foundation], Load method [Media Foundation], IMFTopoLoader interface, Load,IMFTopoLoader.Load, mf.imftopoloader_load, mfidl/IMFTopoLoader::Load
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFTopoLoader.Load
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFTopoLoader::Load method


## -description



          Creates a fully loaded topology from the input partial topology.
        


## -parameters




### -param pInputTopo [in]

A pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the partial topology to be resolved.


### -param ppOutputTopo [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the completed topology. The caller must release the interface.


### -param pCurrentTopo [in]


            A pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the previous full topology. The topology loader can re-use objects from this topology in the new topology. This parameter can be <b>NULL</b>. See Remarks.
          


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
One or more output nodes contain <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointers. The caller must bind the output nodes to media sinks. See  <a href="https://msdn.microsoft.com/d4f93f34-0af1-431f-9333-70ea09691b64">Binding Output Nodes to Media Sinks</a>.

</td>
</tr>
</table>
 




## -remarks




        This method creates any intermediate transforms that are needed to complete the topology. It also sets the input and output media types on all of the objects in the topology. If the method succeeds, the full topology is returned in the <i>ppOutputTopo</i> parameter.
      


        You can use the <i>pCurrentTopo</i> parameter to provide a full topology that was previously loaded. If this topology contains objects that are needed in the new topology, the topology loader can re-use them without creating them again. This caching can potentially make the process faster. The objects from <i>pCurrentTopo</i> will not be reconfigured, so you can specify a topology that is actively streaming data. For example, while a topology is still running, you can pre-load the next topology.
      


        Before calling this method, you must ensure that the output nodes in the partial topology have valid <a href="https://msdn.microsoft.com/fe403cab-b901-4c8e-a23c-788ee65c4689">IMFStreamSink</a> pointers, not <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointers. The Media Session automatically performs this action inside the <a href="https://msdn.microsoft.com/ea5313f0-b0fd-4945-97a2-b3f17937294f">IMFMediaSession::SetTopology</a> method. However, if you call <b>Load</b> before calling <b>SetTopology</b>, you must bind the output nodes manually. For more information, see <a href="https://msdn.microsoft.com/d4f93f34-0af1-431f-9333-70ea09691b64">Binding Output Nodes to Media Sinks</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/66aa07d8-6756-4d5b-9f0a-24b902da6fa2">Advanced Topology Building</a>



<a href="https://msdn.microsoft.com/5ebf117c-e60a-40f2-a24b-c4f9dbdae942">IMFTopoLoader</a>



<a href="https://msdn.microsoft.com/6fc19244-0f42-4d23-899d-c79e97018855">Topologies</a>
 

 

