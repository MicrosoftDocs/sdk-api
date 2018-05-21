---
UID: NF:mfidl.IMFMediaSession.SetTopology
title: IMFMediaSession::SetTopology
author: windows-driver-content
description: Sets a topology on the Media Session.
old-location: mf\imfmediasession_settopology.htm
old-project: medfound
ms.assetid: ea5313f0-b0fd-4945-97a2-b3f17937294f
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: IMFMediaSession interface [Media Foundation],SetTopology method, IMFMediaSession.SetTopology, IMFMediaSession::SetTopology, SetTopology, SetTopology method [Media Foundation], SetTopology method [Media Foundation],IMFMediaSession interface, ea5313f0-b0fd-4945-97a2-b3f17937294f, mf.imfmediasession_settopology, mfidl/IMFMediaSession::SetTopology
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
-	IMFMediaSession.SetTopology
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaSession::SetTopology


## -description



          Sets a topology on the Media Session.
        


## -parameters




### -param dwSetTopologyFlags [in]


            Bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/2993bdf9-cf28-4e20-9f38-f51fb0f6429e">MFSESSION_SETTOPOLOGY_FLAGS</a> enumeration.
          


### -param pTopology [in]


            Pointer to the topology object's <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface.
          


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">

                The operation cannot be performed in the Media Session's current state.
              

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TOPO_INVALID_TIME_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The topology has invalid values for one or more of the following attributes:

<ul>
<li>
<a href="https://msdn.microsoft.com/a2a64cac-0dc1-41b0-b59c-a477c7304ba1">MF_TOPONODE_MEDIASTART</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c1022538-ea9f-41e9-9075-c106e8b16b7b">MF_TOPONODE_MEDIASTOP</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7669f97e-87ad-4a64-a2a5-62b8ce450d80">MF_TOPOLOGY_PROJECTSTART</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1ca3709e-88ea-40ca-8da4-c2259365122b">MF_TOPOLOGY_PROJECTSTOP</a>
</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_DRM_DEBUGGING_NOT_ALLOWED</b></dt>
</dl>
</td>
<td width="60%">

                Protected content cannot be played while debugging.
              

</td>
</tr>
</table>
 




## -remarks




        If <i>pTopology</i> is a full topology, set the <b>MFSESSION_SETTOPOLOGY_NORESOLUTION</b> flag in the <i>dwSetTopologyFlags</i> parameter. Otherwise, the topology is assumed to be a partial topology. The Media Session uses the topology loader to resolve a partial topology into a full topology.

If the Media Session is currently paused or stopped, the <b>SetTopology</b> method does not take effect until the next call to <a href="https://msdn.microsoft.com/1bdec0c0-b042-4e5e-a72b-b15942750ced">IMFMediaSession::Start</a>.

If the Media Session is currently running, or on the next call to <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>, the <b>SetTopology</b> method does the following:

<ul>
<li>If the <b>MFSESSION_SETTOPOLOGY_IMMEDIATE</b> flag is set in <i>dwSetTopologyFlags</i>, the Media Session ends the current presentation immediately, clears all pending topologies, and uses <i>pTopology</i> to start a new presentation.</li>
<li>Otherwise, the Media Session queues <i>pTopology</i> and starts the new presentation when the current presentation has completed. If there is no current presentation, the new presentation starts immediately.</li>
<li>Starting in Windows 7, you can also specify the <b>MFSESSION_SETTOPOLOGY_CLEAR_CURRENT</b>  flag to clear the current topology but leave any other pending topologies on the queue.</li>
</ul>

        This method is asynchronous. If the method returns S_OK, the Media Session sends an <a href="https://msdn.microsoft.com/22a298b7-d32b-44ed-b0a1-4e0398ecfe04">MESessionTopologySet</a> event when the operation completes.
      If the Media Session is currently paused to stopped, the Media Session does not send the MESessionTopologySet event until the next call to <a href="https://msdn.microsoft.com/1bdec0c0-b042-4e5e-a72b-b15942750ced">IMFMediaSession::Start</a>





## -see-also




<a href="https://msdn.microsoft.com/feebf891-73fa-4fe6-94ca-3594986fc92d">IMFMediaSession</a>
 

 

