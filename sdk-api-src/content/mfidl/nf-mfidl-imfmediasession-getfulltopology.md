---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IMFMediaSession::GetFullTopology


## -description



          Gets a topology from the Media Session.

This method can get the current topology or a queued topology.


## -parameters




### -param dwGetFullTopologyFlags [in]


            Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/a635b9c8-f01f-4757-8dc2-f470c2270efa">MFSESSION_GETFULLTOPOLOGY_FLAGS</a> enumeration.
          


### -param TopoId [in]

The identifier of the topology. This parameter is ignored if the <i>dwGetFullTopologyFlags</i> parameter contains the <b>MFSESSION_GETFULLTOPOLOGY_CURRENT</b> flag. To get the identifier of a topology, call <a href="https://msdn.microsoft.com/f7d33d20-1b58-4b88-9a98-1004a5c42dfa">IMFTopology::GetTopologyID</a>.
          


### -param ppFullTopology






#### - ppFullTopo [out]


            Receives a pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the topology. The caller must release the interface.
          


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




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>



<a href="https://msdn.microsoft.com/a6d9246a-0cc6-4dbd-affa-e7d0bbddb008">TOPOID</a>
 

 

